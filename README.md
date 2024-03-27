# SensorSimPredictor
This project aims to explore the usage of ML Techniques to predict sensor data in a simulated environment.

## Problem Statement
Sensors in cars may fail to transmit temporarily due to various reasons. In order for the car to function as intended
during these outages, we need to accurately predict the data output by those sensors with reliable accuracy.

## Approach
- The training data was collected from [SensorSim](https://github.com/snuc-delta/khackssim).
- SensorSim uses CARLA, a popular simulator for autonomous driving research, to simulate minimal sensor data.
- It uses either Physics-based or probabilistic approaches to calculate data for individual sensors which are not provided by CARLA.
- The data is then stored in a CSV file, which are used to train Regression and Classification models for Engine RPM and Current Gear respectively.

## Usage
- Clone this repository
- Install the required packages using 
  ```shell
  pip install -r requirements.txt
  ```
- Run the iPython Notebooks in your preferred IDE

## Implementation
- This project can accurately predict the data for the following systems.
  - [Engine RPM](train_rpm.ipynb)
    - Random Forest Regressor - **Accuracy: 98%**
    - Linear Regression - **Accuracy: 96%**
    - Support Vector Regressor (no fine-tuning) - **Accuracy: 0%**
    - Support Vector Regressor (Grid Search) - **Accuracy: 98%**
  - [Current Gear](train_gear.ipynb)
    - Random Forest Classifier - **Accuracy: 99%**
    - Multilayer Perceptron - **Accuracy: 99%**
    - Support Vector Classifier - **Accuracy: 99%**

## Conclusion
### We can conclude that:
- Random Forest Regressor is the best model for predicting Engine RPM.
- Random Forest Classifier and Multilayer Perceptron are the best models for predicting the current gear of the engine.
- Support Vector Regressor without GridSearch is not feasible for predicting Engine RPM
- Support Vector Regressor performs much better after fine-tuning hyperparameters using GridSearch

## Credits
- [SensorSim](https://github.com/snuc-delta/khackssim)
- [CARLA](https://carla.org/)
- [Mahasvan](http://github.com/Mahasvan/)
