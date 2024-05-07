# Firebase Data Display

This project showcases real-time data display from Firebase in an HTML webpage. It comprises two essential files:

- **index.html**: This HTML file is responsible for rendering the sensor data on the webpage.
- **app.js**: This JavaScript file configures Firebase and updates the sensor data displayed in the HTML.

## Getting Started

To run this project successfully, you need to set up a Firebase project and configure it with your Firebase credentials. Follow these detailed steps:

1. **Create a Firebase Project**:
   - Visit the [Firebase Console](https://console.firebase.google.com/).
   - Create a new project or use an existing one.
     
# `How To Configure Firebase with Raspberry Pi:`

# `Goto this link `https://console.firebase.google.com/ 

![image](https://user-images.githubusercontent.com/63813881/175879197-5fc94fdd-0a79-4194-9856-976b04acc7be.png)

![image](https://user-images.githubusercontent.com/63813881/175879612-9c757997-4c17-4ebd-9624-0f575602e014.png)

![image](https://user-images.githubusercontent.com/63813881/175879472-99d320da-39a9-471a-baa3-83d44fbe4aaf.png)

# `Then press continue`

![image](https://user-images.githubusercontent.com/63813881/175879924-81169b80-7f8b-4977-ba5e-986241b50035.png)

# `Then press continue`

![image](https://user-images.githubusercontent.com/63813881/175880305-a0616d07-e968-4ebb-87b7-ca11f8cf4393.png)

# `Then Click Create Project`

![image](https://user-images.githubusercontent.com/63813881/175880541-2c774cc6-e107-4a28-840a-54601fd65d4d.png)

![image](https://user-images.githubusercontent.com/63813881/175880616-143e79dc-94a7-40f0-b229-ec674848dad8.png)

# `Our project is ready to use Press Continue`

# `You directly redirect to firebase console`

![image](https://user-images.githubusercontent.com/63813881/175880787-8e4e80e0-0d0d-41d0-9272-bf94808f04a2.png)

![image](https://user-images.githubusercontent.com/63813881/175881056-8cb203aa-526c-42a7-adf9-8a0e67826e18.png)

# `After Click Build Button You Can See Realtime Database Just Click There`

![image](https://user-images.githubusercontent.com/63813881/175881311-a3d75878-b1f8-4fc2-b0b9-847e8483d804.png)

# `Now You Directly Redirect Realtime Database`

![image](https://user-images.githubusercontent.com/63813881/175881689-9c6a0d84-5d0a-4c5f-8162-df8396069ebb.png)

# `Click Create Database`

![image](https://user-images.githubusercontent.com/63813881/175881856-da02d10c-de48-46e8-8769-d9bec7a195ae.png)

# `After clcik create Database then Click On Next button`

![image](https://user-images.githubusercontent.com/63813881/175882097-e610a80c-1f57-4e3e-a16f-20da5d63b1b0.png)

# `Make sure you on test mode only`

![image](https://user-images.githubusercontent.com/63813881/175882255-ce8fc6d9-7530-4122-9ec2-fb41887b4b70.png)

# `Press Enable Button`

![image](https://user-images.githubusercontent.com/63813881/175882354-9807b2f8-3c41-4a26-8a3a-c39d6910c93c.png)

# `Database is created Successfully`

![image](https://user-images.githubusercontent.com/63813881/175882768-ea2b196a-2dd0-4cf1-b51d-c3cb41ae34c8.png)

# `One more thing is here go "Project Overview"`

![image](https://user-images.githubusercontent.com/63813881/175882952-c8f5d99a-7b53-4ba9-bc81-dd734ccc6445.png)

# ` Click web button`

![image](https://user-images.githubusercontent.com/63813881/175883120-72dbc675-eef2-4257-bd2a-0c703e4e4278.png)

# `Enter Web App Name`

![image](https://user-images.githubusercontent.com/63813881/175883314-6a45bbc7-be74-4caa-b590-fb5fc7391afe.png)

# `Like This`

![image](https://user-images.githubusercontent.com/63813881/175883442-12059ce3-86fc-4c08-b3c0-9c63a1d66452.png)

# `click on Button`

![image](https://user-images.githubusercontent.com/63813881/175883314-6a45bbc7-be74-4caa-b590-fb5fc7391afe.png)

# `Copy this thing into the code`

![image](https://user-images.githubusercontent.com/63813881/175884009-796b4d0c-bcea-4569-9771-eba07fcfc72d.png)

2. **Configure Firebase**:
   - In your Firebase project, navigate to Project Settings.
   - Under the "General" tab, find your Firebase configuration object.

### Firebase Configuration

In the `app.js` file, replace the placeholder Firebase configuration object with your actual Firebase configuration. This includes your API key, authentication domain, database URL, and other necessary details.

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    databaseURL: "YOUR_DATABASE_URL",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID",
    measurementId: "YOUR_MEASUREMENT_ID"
};
```

3. **Include Firebase SDK**:
   - In the `index.html` file, include the Firebase SDK scripts. This project utilizes Firebase Realtime Database, so ensure to include `firebase-app.js` and `firebase-database.js` scripts.

```html
<!-- Firebase SDK -->
<script src="https://www.gstatic.com/firebasejs/7.14.6/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/7.14.6/firebase-database.js"></script>
```

## How It Works

### Database Structure

This project assumes the Firebase Realtime Database is structured as follows:

```
tuesday-class-acf4f
│
└── Sensor
    ├── sensor1
    │   ├── data: value
    │   └── timestamp: value
    └── sensor2
        ├── data: value
        └── timestamp: value
```

### JavaScript Logic

- **Initializing Firebase**: `app.js` initializes Firebase with the provided configuration.
- **Database Reference**: It obtains references to two nodes in the database: `Sensor/sensor1` and `Sensor/sensor2`.
- **Updating Sensor Data**: Two functions, `updateSensor1Data()` and `updateSensor2Data()`, are responsible for updating the HTML with real-time sensor data.
- **Listening for Changes**: The script listens for changes to the sensor data using Firebase's `on()` method and updates the HTML accordingly.

## Running the Project

To view real-time sensor data, simply open the `index.html` file in a web browser.


## Files Included

- **index.html**: HTML file for sensor data display.
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Firebase Data Display</title>
</head>

<body>
    <h1>Sensor Datas</h1>
    <div id="sensor1Data"></div>
    <div id="sensor2Data"></div>

    <!-- Firebase SDK -->
    <script src="https://www.gstatic.com/firebasejs/7.14.6/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/7.14.6/firebase-database.js"></script>
    <script src="app.js"></script>

</body>

</html>
```
- **app.js**: JavaScript file for Firebase configuration and data update logic.

```javascript
// Firebase configuration
const firebaseConfig = {
    apiKey: "AIzaSxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    authDomain: "tuesday-cxxxxxxxxx.firebaseapp.com",
    databaseURL: "https://tuesday-cxxxxxxxxxxxxxxxxxxxx.firebaseio.com",
    projectId: "tuesday-cXxxxxxxxxxxxxxx",
    storageBucket: "tuesday-cxxxxxxxxxxxx.appspot.com",
    messagingSenderId: "373xxxxxxxxxx",
    appId: "1:3734Xxxxxxxxxxx:web:6a715a4xxxxxxxxxxx",
    measurementId: "G-6RDxxxxxxxxx"
};

// Initialize Firebase
const app = firebase.initializeApp(firebaseConfig);
console.log("Firebase initialized:", app);

// Get a reference to the database
const db = firebase.database();
console.log("Database reference:", db);

// Get a reference to the database nodes
const sensor1Ref = db.ref('Sensor');
const sensor2Ref = db.ref('Sensor');

// Function to update sensor 1 data in HTML
function updateSensor1Data(data) {
    document.getElementById('sensor1Data').innerHTML = "<p><strong>Sensor 1 Data:</strong> " + JSON.stringify(data) + "</p>";
}

// Function to update sensor 2 data in HTML
function updateSensor2Data(data) {
    document.getElementById('sensor2Data').innerHTML = "<p><strong>Sensor 2 Data:</strong> " + JSON.stringify(data) + "</p>";
}

// Listen for changes to sensor 1 data
sensor1Ref.on('value', (snapshot) => {
    const data = snapshot.val();
    console.log("Sensor 1 Data:", data);
    updateSensor1Data(data);
});

// Listen for changes to sensor 2 data
sensor2Ref.on('value', (snapshot) => {
    const data = snapshot.val();
    console.log("Sensor 2 Data:", data);
    updateSensor2Data(data);
});
```

## Output:
![image](https://github.com/MuhammadRaheelNaseem/Fetch-Data-From-Firebase/assets/63813881/9aac5269-5ff9-45ea-8c32-4986aca72f16)
