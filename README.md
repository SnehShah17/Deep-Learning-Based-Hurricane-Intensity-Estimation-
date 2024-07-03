
<p align="center">

  <h2 align="center">Deep Learning Based Hurricane Intensity Estimation</h2>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#dataset-used">Dataset Used</a></li>
      <li><a href="#technology-used">Technology Used</a></li>
      <li><a href="#model-training">Model Training</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Employed an innovative approach to extract crucial insights from National Hurricane Center’s HURDAT2 database for recent years (2019, 2018, 2017, 2016 and 2015) enabling precise hurricane intensity forecasts. 
Implemented a 5-layer Convolutional Neural Network (CNN) while harnessing a diverse range of performance metrics to comprehensively assess and refine predictive capabilities of engineered model.
### Technology Used

* Python
* TensorFlow
* CNN

### Dataset Used
Data scraping was used to obtain hurricane imaging data from the HURSAT data project for recent years (2019, 2018, 2017, 2016, and 2015). 
The process involved scraping a website to acquire files, including satellite photos for each storm. 
The algorithm filtered the data to focus on hurricanes in the Atlantic and Pacific basins, which had wind speed and position records in the National Hurricane Center’s Best Track dataset. 
NetCDF files containing satellite images of each hurricane were then extracted and saved locally. 
Additionally, wind speeds of these hurricanes, recorded at 6-hour intervals, were included. New images and corresponding labels were also generated using image augmentation techniques

### Model Training

* The architecture of the constructed model, which was intended to predict a continuous value for grayscale images, comprised three convolutional layers and a fully connected neural network.
* The rmsprop optimizer was used for model optimization, with the mean squared error loss function. During training, this optimizer adjusted the network’s weights to minimize loss
* During training, the model calculated two metrics to evaluate its performance on the training set: mean absolute error and root mean squared error.
* The model’s performance on the validation set was reviewed after each epoch to check for overfitting. An EarlyStopping callback was used to halt training if the validation error did not improve after a certain number of epochs.

### Conclusion
CNNs can efficiently predict hurricane intensity, potentially mitigating significant consequences through timely action.
