## Configuration Examples

### Simulator Configuration
Configures the material properties for the elements in the simulation such as the road, concrete, steel ,etc. Also configures the maximum number of cars on the road and the rate at which they are spawn. 

```json
{
  "id": "simulator_test",
  "server_ip": "127.0.0.1",
  "server_port": 8999,
  "simulation_mode": 0,
  "phys_materials": {
    "Aluminum": {
      "specular_exponent": 15.0,
      "specular_coefficient": 0.95,
      "diffuse_coefficient": 0.26,
      "dielectric_constant": 10.0,
      "roughness": 0.15
    },
  ...
  },
  "traffic_configuration": {
    "max_vehicles": 40,
    "spawn_rate": 0.25
  },
  "client_settings": {
    "map": {
      "gis_anchor": { "x": 0, "y": 0, "z": 0},
      "point_delta": 100.0
    }
  }
}
```
<p>&nbsp;</p>



### Sensor Configuration

<p class="img_container">
<img class="lg_img" src="https://github.com/monoDriveIO/client/raw/master/WikiPhotos/LV_client/sensors/mono__camerac.png"/>
</p>

To change the configuration of any sensor, double-click on the sensor subVI and make the changes you need. 
Make sure you save the configuration as default value so that is persistent the next time you open your application.

<div class="img_container">
    <img class='lg_img' src="../imgs/sensor_file.png"/>
</div>

   **NOTE:**
   Make sure the “listen_port” chosen is not used by another process or sensor.

<p>&nbsp;</p>


### Sensor Output
Double-click on each sensor to look at the output of each sensor while running.

<div class="img_container">
    <img class='lg_img' src="https://github.com/monoDriveIO/documentation/raw/master/docs/LV_client/quick_start/imgs/output1.png"/>
</div>

<div class="img_container">
    <img class='lg_img' src="https://github.com/monoDriveIO/documentation/raw/master/docs/LV_client/quick_start/imgs/output2.png"/>
</div>

<p>&nbsp;</p>


### Add Sensors
The easiest way to add a new sensor to your application is to create a copy of the sensor you need (on your directory explorer). Change the port for communication for the second sensor. 
Then grab and drop the second sensor into your application and connect appropriately.

<div class="img_container">
    <img class='wide_img' src="https://github.com/monoDriveIO/documentation/raw/master/docs/LV_client/quick_start/imgs/add_sensor.png"/>
</div>

<p>&nbsp;</p>


### Trajectory Configuration File
The client ships with some sample trajectory files, usually under 
*C:\Program Files\National Instruments\LabVIEW 2019\vi.lib\monoDrive\monoDriveClient\labview\trajectories*

<p>&nbsp;</p>

<p class="img_container">
<img class="lg_img" src="https://github.com/monoDriveIO/client/raw/master/WikiPhotos/LV_client/utilities/mono__send__trajectoryc.png"/>
</p>

<p>&nbsp;</p>


```json
[
   {
       "frame": [
           {
               "angular_velocity": [
                   -2.444333949824795e-05,
                   0.005100168287754059,
                   0.0002663454506546259
               ],
               "name": "ScenarioVehicle_1",
               "orientation": [
                   -0.0001492226729169488,
                   1.4324657968245447e-05,
                   -0.7113564014434814,
                   0.702831506729126
               ],
               "position": [
                   15015.98828125,
                   15328.6845703125,
                   15.90130615234375
               ],
               "steering_direction": 0.305339515209198,
               "tags": [
                   "vehicle",
                   "dynamic",
                   "ego"
               ],
     "velocity": [
                   -0.6869845390319824,
                   -1.3215781450271606,
                   -37.32944107055664
               ]
           },
           {
               "angular_velocity": [
                   -0.02693433128297329,
                   -0.030446365475654602,
                   0.00673380121588707
               ],
               "name": "ScenarioVehicle2",
               "orientation": [
                   -0.0005045104771852493,
                   0.0001808821689337492,
                   0.7072895169258118,
                   0.7069238424301147
               ],
               "position": [
                   13788.91796875,
                   15402.078125,
                   15.537322998046875
               ],
               "steering_direction": -0.042938876897096634,
       "tags": [
                   "vehicle",
                   "dynamic"
               ],
               "velocity": [
                   1.838138461112976,
                   656.9227294921875,
                   -40.23637390136719
               ]
           }
...
          
```
               
<p>&nbsp;</p>


### Weather Configuration 

```json
{
 "set_profile": "CloudySunset",
 "profiles": [
 "id": "Default",
 "SunPolarAngle": 44.586,
 "SunAzimuthAngle": 174,
 "SunBrightness": 50,
 "SunDirectionalLightIntensity": 15.092,
 "SunDirectionalLightColor": {
    "R": 255.0,
    "G": 239.0,
    "B": 194.0,
    "A": 1.0
    },
 "SunIndirectLightIntensity": 6,
 "CloudOpacity": 16.296,
 "HorizontFalloff": 3,
 "ZenithColor": {
       "R": 0.034046,
       "G": 0.109247,
       "B": 0.295,
       "A": 1.0
     },
 "HorizonColor": {
     "R": 0.659853, "G": 0.862215, "B": 1.0, "A": 1.0
 },
 "CloudColor": {
       "R": 0.855778, "G": 0.919005, "B": 1.0, "A": 1.0
     },
     "OverallSkyColor": {
       "R": 1.0, "G": 1.0, "B": 1.0, "A": 1.0
     },
     "SkyLightIntensity": 5.505,
     "SkyLightColor": {
       "R":0.149650, "G":0.161819, "B":0.205000, "A":0.000000
     },
     "bPrecipitation": false,
     "PrecipitationType": "Rain",
     "PrecipitationAmount": 0,
     "PrecipitationAccumulation": 0,
     "bWind": false,
     "WindIntensity": 20,
     "WindAngle": 0,
     "bOverrideCameraPostProcessParameters": true,
     "CameraPostProcessParameters": {
         "AutoExposureMethod": "Histogram",
         "AutoExposureMinBrightness": 0.27,
         "AutoExposureMaxBrightness": 5,
         "AutoExposureBias": -3.5
     }
... 
]
```


<p>&nbsp;</p>


### Errors
If an error occurred during the execution, the error cluster will give you information on the error.


<div class="img_container">
    <img class='lg_img' src="../imgs/error.png"/>
</div>

<p>&nbsp;</p>
