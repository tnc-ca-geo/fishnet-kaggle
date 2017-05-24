## Kaggle to Production steps/packaging

### 1. Enhanced training data

- Apply lessons learned from Kaggle competition to improve training/test data sets for production model training 
- Balanced species distribution
- More images of sensitive conservation relevant species e.g. sharks, turtles, etc.
- Better distribution of ships
- Third party data
- Other lessons learned from competition results and forums

### 2. Data augmentation pipeline

Data augmentation proofed to be the single most important step to boost competition results:

- Create simple modular Python pipeline that can apply all data augmentation steps automatically and that allows for quick changes of steps and treatments.
- Apply augmentations that proofed successful during the Kaggle competition
- Deliverable: simple Python module that can be called like this:

```
$ augment_data --input_folder {foldername} --output_folder {foldername) --label_file {filename} --new_label_and_weights_file {filename} 
```

### 3. Package all model dependencies 

- Create an easily reproducable route to create an environment in which a) models can be trained, b) deployed. Options would be 1. provisioning tools like (Ansible, Chef, Puppet, and the like), 2. Docker containers, or 3. prepackaged server images with all the relevant products installed (most likely a combination of 1 and 3), or readily available cloud servers.

### 4. Create and train fish detection model

During the competition explicit fish detection models proofed to be more successful then implicite object classification algorithms as build into some of the applied model products. If we decide to implement a two step recognition process (1. fish, 2. species). Retrain model and deploy that it can be run as:

```
$ create_fish_images --input_folder --output_folder
```

Label files should be unaffected.

### 5. Setup easy workflow for fast retraining of models

- Create simple command line writer for retraining models.
- Allow for plug and play of different models
- Goal should be to find the single best performaing model (with potential trade-offs for speed)

### 6. Create command line interface for speedy model application

- This form allows for implementation in a wide range of context 
- A verbose version could provide more context information

```
$ classify --image {imagename}

['ALB']
```

### 7. Create simple web application that provides an online interface to 6

Something like:

```
curl -X POST fish.org/classify --data-binary=/path/to/image  
```

- Interface should match Camio's requirements.
