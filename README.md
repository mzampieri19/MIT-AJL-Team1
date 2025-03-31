# MIT-AJL-Team1
Equitable AI for Dermatology Team 1

**Team Members:**
[Karen Bei](https://github.com/kbei5234), 
[Isabelle Wang](https://github.com/isabellelwang),
[Michelangelo Zampieri](https://github.com/mzampieri19),
[Humaira Sarwary](https://github.com/humairasarwary),
[Natalie Cheng](https://github.com/nataliemcheng)

__________________________________________________________________________

**Project Highlights**

- Built a CNN using many layers, pooling, and learning rates to classify different skin conditions
- Achieved 37st on the final Kaggle Leaderboard
- Used Tensorflow libraries to interpret model decisions
- Implemented horizontal and vertical shifts, scaling, rotations, and reflections to optimize results within compute constraints
_________________________________________________________________________

**Setup and Execution**

Files in this Github:

- AJL_Team1_Submission1.csv. Our first submission file.

- AJL_Team1_Submission2.csv. Our second submission file.

- README. This file

- best_fine_tuned_model.h5. Saves the updated model.

- my_model.h5. Saves the model and its parameters to make it easier to load in the future (no need to train it everytime).

- pre-processing.ipynb. This notebook checks the original data, and does some basic exploration. Then it augments the images in the training dataset to provide more training images.

- predictions.csv. A CSV file of the model's predictions (what we would submit).

- training.ipynb. In this notebook a CNN model is prepared and trained.

To run the pre-processing and training notebooks, download the files and open them in your desired workspace. After that, you should be able to run all the cells like any other jupyter notebook. 
_________________________________________________________________________

**Project Overview** 
The project aims to increase awareness for the harmful social implications of AI and reduce significant discriminatory threats. 

Competition Overview: 
This Kaggle Competition aims to put the machine learning skills learned over the past year into a more practical setting. We see the importance of preparing a quality data set, training it, and fine tuning our model to meet real world needs. 

Real World Impact: 
The model should classify skin conditions across diverse skin tones to increase fairness in dermatology and ensure that historically underrepresented groups deserve fair treatment. 

Competition Objectives: 
- Create a model that is able to classify 21 various skin conditions across a range of skin tones
- Document the process to tie technologies and model back to the real world impact

Overall Team Goals:
- Create working model first then fine tune for optimization.
- Achieve top 10 rank
- Everyone works on things they are familiar and unfamiliar with

__________________________________________________________________________

**Data Exploration**
We used the data provided on the Kaggle. From their description, "About 4500 images are in this set, representing 21 skin conditions out of the 100+ in the full FitzPatrick set."

Data Processing:
The main data processing we did for this process was data augmentation and resizing. For data augmentation we did most of the basic operations, zoom in/out, brightness changess, rotations, and shifting. We also resized all images to (244, 244) for more consistancy. After this step, we created 25740 images from the original 2860 images. Each category has 9x the number of images what it had initially.  We made sure to prepare the images through a variety of transformations because the conditions look different on everyone, so we wanted to increase the diversity of data that our model was seeing. 

Visualizations:
Visualization 1
![Data Exploration 1](data_exploration1.png)

Visualization 2
![Data Exploration 2](data_exploration2.png)
__________________________________________________________________________

**Model Development**

We used a CNN to create our prediction data. We split up our data to be 80% training and 20% validation. We would fine tune the model by adding more epochs and slow down the training. We noticed that the training and validation accuracy increased the more we trained it, which was what we expected. 

__________________________________________________________________________

**Results & Key Findings**

Our initial model had an accuracy of 0.32.
__________________________________________________________________________

**Impact Narrative**
1. What steps did you take to address model fairness?
   
   We made sure to scale all the images so that there was plenty across the board. Also, by scaling each one to the same size, we limit the amount of information that can be conveyed, which helps the model to focus on the category rather than adding extra information that could lead to biases. 
   
3. What broader impact could your work have?
   
   Our work could be relevant beyond the scope of the project because there are many factors to consider before deploying a new model for public use. We've started to identify how we would like to approach it and what developers can do to ensure equity. It goes to show how interdiscplinary AI/ML is because we need to consider social implications of the technology or how it may be used in various audiences. 
__________________________________________________________________________

**Next Steps & Future Improvements**

With more time, we think it would be interesting to add filters to slightly change the skin colors and create a bit more data. We would also hope to train the model more since it takes quite a bit to get a model. 
