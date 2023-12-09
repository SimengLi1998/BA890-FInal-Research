# Advertising Video Analysis

# BA890 Final Research

-   Name: Simeng Li
    
-   Email:  [simone@bu.edu](mailto:simone@bu.edu)
    
-   BU ID: U01878286
    

## Write in Front

1. Colab Link: [https://colab.research.google.com/drive/1qepZI_rv1MDq3wX_r-59yqQCGR0mLyOl?usp=sharing](https://colab.research.google.com/drive/1qepZI_rv1MDq3wX_r-59yqQCGR0mLyOl?usp=sharing)

2. Google Drive Link: Running DeepFM is out of memory in the colab chunk, I have trained the model in the local Pycharm IDE and saved the DeepFM model and the environment into Google Drive. [https://drive.google.com/drive/folders/1n_v8mlqWkoogXYiKTCdTAFc1XPQcgLWr?usp=sharing](https://drive.google.com/drive/folders/1n_v8mlqWkoogXYiKTCdTAFc1XPQcgLWr?usp=sharing)

3. Environment to Local Pycharm IDE:
	-   Python 3.7.0
	-   Tensorflow 2.8.0
    

  
  

## Initial Proposal

### 1. Background & Motivation

A good advertisement can attract customers to click, convert and even pay. So what makes a good advertisement? It should be an advertisement with a high click rate and a high ROI. However, making a good ad is pretty hard and unpredictable, and even the people who create these successful ads don't know why. How can we identify good ads, enlarge the budget, and win higher user recovery? At the same time, how can we identify ineffective ads and save the company's budget? Based on this business problem, I want to use the machine learning method to learn the complex logical structure of advertisements, and the final result will be to realize the binary classification of excellent advertisements.

### 2. Data Introduction

The dataset is from online video advertisements. These videos are dedicated to attracting gamers. It includes 16 columns and 8980 rows.

Link: [https://github.com/SimengLi1998/Data/blob/main/ori_data.txt](https://github.com/SimengLi1998/Data/blob/main/ori_data.txt)

**Video Intrinsic Features:**

| Feature           | Description                        |
|-------------------|------------------------------------|
| Material_id       | Video ID                           |
| Label_ids         | Element IDs used in the video      |
| V_resolution_id   | Resolution of the video            |
| Duration          | Length of the video                |
| r_frame_rate      | Video frame rate                   |
| Display_type      | View in landscape or portrait      |
| Path              | Video path                         |

**Video Effects Features:**

| Feature           | Description                                |
|-------------------|--------------------------------------------|
| Avg_cost          | Average cost per serving                   |
| Ctr               | Average click rate                         |
| Cvr               | Average converted rate                     |
| Ecpm              | Effective cost per mille                   |
| Deep_convert_rate | Deep converted rate                        |
| Pay_rate          | Average pay rate                           |
| First_day_roi     | First day Return on Investment (ROI)      |
| Valid_play_rate   | Rate of successfully played videos        |
| Finish_play_rate  | Rate of successfully finished viewing     |


    

### 3. Steps & Milestones
-   Manual labeling：
	-   According to the Video effects features, find out the reasonable evaluation criteria for good video, above the standard is "1", below the standard is "0"
  
-   Extract video features：
    

	-   Download the video, and extract the key frame information and audio features in the video;
    

-   Sklearn models:
    

	-   Run the baseline by using Randomforest / KNN / LogisticRgression / SVM / MLP classifiers ;
    

-   Explore better classifiers:
    

	- Try to fit the data with Wide&Deep model and DeepFM model to improve the classification.

