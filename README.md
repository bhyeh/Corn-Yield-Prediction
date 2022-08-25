# Corn Yield Estimation from High Resolution UAS Imagery

## Page Description 
An **_extremely brief_** showcase of my ongoing work and early research results @ Cornell's Nutrient Management Spear Program (NMSP) and their Digital Agriculture initiative. If you are interested in more details or obtaining a preprint, please reach out to me @ **by253@cornell.edu**! 

[Click here to jump to visuals](#visual-results)

## Research Objective 
Within-field yield measurements obtained by yield monitor systems offer powerful insight to improving allocation of crop inputs and farm resources. Specifically, access to yield and its variability can aid in precisely addressing Nitrogen needs throughout a field, reducing both the financial and environmental costs associated with excess Nitrogen use. However, existing yield monitor systems can be expensive, data collection is tedious requiring delicate calibration, and post-harvest data cleaning is a laborious effort. 

The objective of my research is to evaluate whether corn grain and silage yield can be estimated from high resolution unmanned aerial system (UAS) imagery in combination with various neural network architectures such as Long Short Term Memory (LSTM) and Convolutional (CNN) networks.
  
## Data Set 
During the growing season of 2019, weekly color (RGB) and multispectral (RG-NIR) images of eight farm fields (three grain, five silage; ~**420 acres** in total) were collected by a Quantix™ hybrid drone over the span of 13 and 14 weeks. As a result, 8 frame sequences were obtained with approximately 220 frames in total. In addition to the images obtained by the Quantix drone, easily accessible weather and terrain elevation data from the Web were further sourced in constructing the data set. 

## Preliminary Experimentation 

With developing a network, the goal is to model the temporal relationship between weekly drone images to the end of harvest yield. Below are the results of a LSTM based network. 

**Training and Validation:** The entire data set has been carefully partitioned to reflect practical case use. Specifically, the training set consists of **six** distinct farm fields (~355 acres) while an **entire** fifth and sixth field (~65 acres) are held out completely from training for validation and testing. 

### Visual Results

Results from current model experimentation and development below.

![image](https://user-images.githubusercontent.com/89032804/186761196-163e773c-b09f-4e78-8c36-5a3310b64388.png)
