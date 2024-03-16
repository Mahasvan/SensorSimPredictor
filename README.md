# SensorSimPredictor
This project aims to explore the usage of Random Forest Regressor and Classifier to predict sensor data in a simulated environment.

## Idea
Sensors in cars may fail to transmit temporarily due to various reasons. In order for the car to function as intended
during these outages, we need to accurately predict the data output by those sensors with reliable accuracy.

## Approach
- The training data was collected from [SensorSim](https://github.com/snuc-delta/khackssim).
- SensorSim uses CARLA, a popular simulator for autonomous driving research, to simulate minimal sensor data.
- It uses either Physics-based or probabilistic approaches to calculate data for individual sensors which are not provided by CARLA.
- The data is then stored in a CSV file, which are used to train Regression and Classification models.

## Implementation
- This project can accurately predict the data for the following systems.
  - Engine RPM
    - Random Forest Regressor was used to train the model.
    - Accuracy: 98%
  - Current Gear
    - Random Forest Classifier was used to train the model.
    - Accuracy: 97%

## Usage
- Clone this repository
- Install the required packages using 
  ```shell
  pip install -r requirements.txt
  ```

## Credits
- [SensorSim](https://github.com/snuc-delta/khackssim)
- [CARLA](https://carla.org/)
- [Mahasvan](http://github.com/Mahasvan/)
