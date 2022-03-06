# Cornell-Corn-Yield-Prediction

## Repository Description ##
An **_extremely brief_** showcase of my ongoing research and work @ Cornell's Nutrient Management Spear Program (NMSP) and their Digital Agriculture initiative. If you are interested in more details or obtaining a preprint, please reach out to me @ **by253@cornell.edu**! 

## Research Objective ##
Within-field yield measurements obtained by yield monitor systems can offer powerful insight into improving allocation of crop inputs and farm resources. However, existing yield monitor systems are expensive, data collection is tedious requiring delicate calibration, and post-harvest data cleaning is a laborious effort as well. The objective of my research is to evaluate whether corn grain and silage yield can be efficiently estimated from high resolution unmanned aerial system (UAS) imagery in combination with various neural network architectures. 
  
## Data Collection ##
During the growing season of 2019, a Quantix™ hybrid drone and AeroVironment Decision Support System™ (AeroVironment Inc.) collected weekly color (RGB) and multispectral
(RG-NIR) images of various fields over the span of approximately 14 weeks. In total, eight farms were captured (three grain, five silage; ~420 acres in total). In addition to the images obtained from the Quantix drone, weather and terrain elevation data were further sourced in constructing a dataset to model from. With modeling, the specific goal is to map the temporal relationship between weekly drone images, weather measurements, as well as static regional features (digital elevation and landform classes) to the end of harvest yield.

## Preliminary Results ##

**Important Note on Train-Validate-Test Split:** Current development is being done to reproduce practical in-field use as closely as possible. As a result, the data set has been partitioned to appropiately reflect this. Specifically, the training set consists of **four** distinct fields (~310 acres) while an **entire** fifth field (~53 acres) is held out completely. This hold out field is partitioned once more into validation and testing. I find this crucially important to emphasis because similar research often misuses a _within field_ split.  

Results from current model experimentation and development below.

![image](https://user-images.githubusercontent.com/89032804/156907835-c90ca06b-49a2-46c1-92c2-f3637f1e3c3d.png)

**Noteable Takeaways:**
