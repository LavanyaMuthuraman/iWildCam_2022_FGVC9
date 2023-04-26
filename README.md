---
# iWildCam 2022 - FGVC9
##### Count the number of animals in a sequence of images
---

**This [iWildCam competition](https://www.kaggle.com/competitions/iwildcam2022-fgvc9/overview) will focus entirely on counting animals. We have prepared a challenge where the training data and test data are from different cameras spread across the globe. The set of species seen in each camera overlap, but are not identical. The challenge is to count individual animals across sequences in the test cameras.**

In this notebook, I provide an overview of the competition and explore the dataset before training a baseline model. Additionally, I conduct further analysis using the trained model. I present **two potential solutions: maximum detections in sequence and using the Object-Tracker-Model.** Finally, I draw some conclusions.

### **Data**

 [The iWildCam 2022 WCS](https://www.kaggle.com/competitions/iwildcam2022-fgvc9/data) training set contains 201,399 images from 323 locations, and the WCS test set contains 60,029 images from 91 locations. These 414 locations are spread across the globe. A location ID (location) is given for each image, and in some special cases where two cameras were set up by ecologists at the same location, we have provided a sub_location identifier. Camera traps operate with a motion trigger and, after motion is detected, the camera will take a sequence of photos (from 1 to 10 images depending on the camera). We provide a seq_id for each sequence, and your task is to count the number of individuals across each test sequence.

This year we are also providing count annotations on 1780 of the 36,292 train sequences (check the metadata/train_sequence_counts.csv file). We hope you will find them useful in building better models. We do not provide any count annotations for the test set.

<img width="800" alt="segmentation" src="https://user-images.githubusercontent.com/109660074/234645822-254a0208-e5e9-45e8-8788-4a0e12dc87b5.png">


---
