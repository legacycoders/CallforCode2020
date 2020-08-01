# PREDICTIVE IRRIGATION for water sustainability

## Short description

### What's the problem?
  Of all the water on Earth, just 3% is fresh water. Agriculture is by far the largest water consumer, accounting for 69% of annual water withdrawals globally. ​

### How can technology help?
  Technology helps getting accurate agricultural data to the farmers at affordable price, preserve historical data and get the best practices followed around world for efficient irrigation.
  
### The idea
  The idea is to build a Cloud based IoT  solution using accurate predictive modelling that helps farmers to determine the current soil moisture and as well as prediction for next 48 hours needed for any crop. It will help farmers to irrigate in efficient way thereby  reducing the usage of fresh water and help the community.
  
  1. IoT devices to collect real time soil moisture data and maintain required Soil moisture level for the crop.
  2. Weather Forecasts based model for irrigation
  3. IoT based Drip Irrigation pump actuator.
  4. Mobile app with user friendly dashboard with current & predicted soil moisture


 ### Demo
 [Demo Link] (https://www.youtube.com/watch?v=t8Jef4Uz6Sk)
 
 ### Solution 
 
 ![solutionArchitecture](https://user-images.githubusercontent.com/68838940/89094853-09b69980-d38e-11ea-8384-ef4f6623384b.png)

#### Solution Components
  Following are the components that are built for this solution.
  
  ##### 1. IBM Watson IoT Platform   
      - The platform helps reading the location, real time soil moisture data from the soil sensors.
        Detailed documentation is available under **CallforCode2020/WatsonIot/IBM Watson IoT Platform service.docx**
        
  ##### 2. IBM Watson Studio with ML
        - This platform uses SoilMoisture dataset which comprises of locaiton, air temp, surface temp, percipitation, humidity and soil moisture to train the model and predicts the soil moisture using Extra Tree Regressor algorithm. Model is deployed in the cloud and exposed as API. With the help of scoring end point the soil mositure prediction can access from any application.
          Detailed documentation is available in CallforCode2020/IBMWatsonStudio/IBM Watson Studio.docx
          
  ##### 3. Open Weather Map API
          - Third party API which provides the forcast for next 48 hours for the give location.
       
  ##### 4. Node-RED Platform  
      - It is our integration platform which connects Iot Platform, ML model, IBM DB2, IBM Push notification and Mobile app.
          Detailed documentation is available in CallforCode2020/NodeRed/Node RED Application.docx
          Code availabe in CallforCode2020/NodeRed/flows.json          
      
  ##### 5. IBM DB2 on cloud
       - This is our RDMS database to hold Soil moisture levels for current & next 48 hours and crop data and its intended level of soil moisture.
         Detaild documentation is available in BM Cloud DB2/IBM DB2 on Cloud .docx
         
  ##### 5. Dashboard 
      - IBM embeded Cognos reporting dashboard for visualization
          CallforCode2020/IBMWatsonStudio/CognosDashboard/
  
  ##### 6. Mobile App
       - A user friendly mobile app which will be used by farmer which have the various dashboards, push notification enabled. Farmer can trigger the pump actuator from mobile app or he    subscribe to automated pump actuator based on the threshold level.
       
  ##### 7. Drip Irrigation pump actuator   
       - IoT based hardware device to actuate the wate pump from the inputs received from IoT platform (trigger manually by farmer or automated)
        


#### Roadmap
     1. Push notification to send notifications to mobile devices
     2. To build a mobile app with necessary dashboards and necessary control options for pump actuator. Feedback system to agency about the behavrioal pattern
     3. IoT based pump acutator.
     
 
