# Neural Network Approaches to Corn Grain and Silage Yield Estimation from High Resolution UAS Imagery

## Page Description ##
An **_extremely brief_** showcase of my ongoing work and early research results @ Cornell's Nutrient Management Spear Program (NMSP) and their Digital Agriculture initiative. If you are interested in more fine details or obtaining a preprint, please reach out to me @ **by253@cornell.edu**! 

## Research Objective ##
Within-field yield measurements obtained by yield monitor systems offer powerful insight to improving allocation of crop inputs and farm resources. Specifically, access to yield and its variability can aid in precisely addressing Nitrogen needs throughout a field, reducing both the financial and environmental costs associated with excess Nitrogen use. However, existing yield monitor systems can be expensive, data collection is tedious requiring delicate calibration, and post-harvest data cleaning is a laborious effort. The objective of my research is to evaluate whether corn grain and silage yield can be feasibly estimated from high resolution unmanned aerial system (UAS) imagery in combination with various neural network architectures such as Long Short Term Memory (LSTM) and Convolutional (CNN) networks.
  
## Data Set ##
During the growing season of 2019, weekly color (RGB) and multispectral (RG-NIR) images of eight farm fields (three grain, five silage; ~**420 acres** in total) were collected by a a Quantix™ hybrid drone over the span of 13 and 14 weeks. As a result, 8 frame sequences were obtained with approximately 220 frames in total. In addition to the images obtained by the Quantix drone, easily accessible weather and terrain elevation data from the Web were further sourced in constructing the data set. 

## Preliminary Results ##

With modeling, the specific goal is to map the temporal relationship between weekly drone images, weather measurements, as well as static regional features (digital elevation and landform classes) to the end of harvest yield. Below are the results of a LSTM based network developed specifically for _silage_ prediction. 

**Important Note on Train-Validate-Test Split:** Current development is being done to replicate practical in-field use as closely as possible, where in production a farmer would upload a sequence of drone obtained images _during_ the growing season and recieve a generated prediction map _before_ harvest. As a result, the entire data set has been carefully partitioned to appropiately reflect this intent. Specifically, the training set consists of **four** distinct fields (~310 acres) while an **entire** fifth field (~53 acres) is held out completely from training. This hold out field is partitioned once more into validation and testing. I find this crucially important to emphasis because similar research often misuses a _within field_ split (e.g., 80% from _each_ available field to train and remaining 20% to test; ask me more about this!). 

Results from current model experimentation and development below.

![image](https://user-images.githubusercontent.com/89032804/156907835-c90ca06b-49a2-46c1-92c2-f3637f1e3c3d.png)

### Striking Takeaways ###

There are a few remarkable resemblances between the actual and predicted yield map, some of which I have highlighted below. We can observe that low yielding patches present in the headlands are captured by the network. Further, quite interesting is the distinct 'dog-like' patch in the upper right corner of the field and the 'tail' pattern that is also expressed within the predicted map. These early results show exciting promise and serve as a benchmark to hopefully improve upon with further development. 

![image](https://user-images.githubusercontent.com/89032804/156932821-575b72df-207c-4906-a8ac-e45ec07b0fe9.png)
