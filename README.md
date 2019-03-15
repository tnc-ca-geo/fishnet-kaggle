## Fishnet
###### Outputs from [Kaggle tuna fisheries competition](https://www.kaggle.com/c/the-nature-conservancy-fisheries-monitoring) sponsored by The Nature Conservancy and Vulcan Technologies.  

This project was done in partnership with Satlink, Archipelago Marine Research, the Pacific Community, the Solomon Islands Ministry of Fisheries and Marine Resources, the Australia Fisheries Management Authority, and the governments of New Caledonia and Palau.

The goal of the competition was to create algorithms that can detect and indentify species of fish in video data collected onboard fishing vessels. These data help to manage the stock better.  Our goal is to broadly share the tools and methods in this space (computer vision, machine learning and fisheries) in an an attempt to foster innovation and ideally scale the practice of video monitoring in fisheries.

The competition ran from November 14, 2016 to April 12, 2017 and had 2,293 teams participate. Directory prefixes correspond to final rank in Kaggle private leaderboard.

### Finalist Code and Documentation
The model / algorithm code is available in each team's director (e.g. 1_TROLL...) as well as presentation slides that describe their approach. 

A great place to start is with this [really nice writeup](https://flyyufelix.github.io/2017/04/16/kaggle-nature-conservancy.html) by Felix Yu (8th place). The [Kaggle discussion boards](https://www.kaggle.com/c/the-nature-conservancy-fisheries-monitoring/discussion) for this project are a good resource as well.

### Video Importer
If you are a fisheries Electronic Monitoring vendor please take a look at our [video importer project](https://github.com/tnc-ca-geo/video-importer). The importer traverses directories to import video as segmented events with correct timestamps and metadata and automates the ingestion of video files so they can be labeled by advanced classifiers running either locally or in the cloud.


