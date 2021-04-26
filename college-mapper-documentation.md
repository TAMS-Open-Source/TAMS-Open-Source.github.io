# College Mapper Documentation

We are glad to see you are interested in the ins-and-outs of college mapper. Please allow us to explain how to get college mapper running locally, so that you can can get started extending the application as you see fit.

## Structure

College Mapper is organized into [client](https://github.com/TAMS-Open-Source/college-mapper-client) and [server](https://github.com/TAMS-Open-Source/college-mapper-api) repositories.

## Running the Application Locally

### Server

First, you should run the server. (Note: the following instructions apply to Unix/MacOS environments only; for Windows, your steps [including those for pip environment] will be a bit different, but follow the same general order.)

1. `cd api`
2. `source env/bin/activate`
3. `pip3 install -r requirements.txt`
4. `python3 main.py`

### Client

#### Configure Firebase

This application uses [Firebase](https://firebase.google.com/) to facilitate authentication and data storage. Thus, to run this application locally, you should create a Firebase project, then make a web app inside the project. After making this web app, you will be a Firebase 'API Key,' as well as several other pieces of information necessary to running this application locally. 

Create a `.env` file in the `/client` directory. You should configure these environment variables to correspond to the data you got from Firebase after making the web app. In the following list, the name of the relevant strings in the `firebaseConfig` object given in your Firebase project settings are given in parentheses.

1. `REACT_APP_API_KEY` (`apiKey`)
2. `REACT_APP_AUTH_DOMAIN` (`authDomain`)
3. `REACT_APP_DATABASE_URL` (`databaseURL`)
4. `REACT_APP_PROJECT_ID` (`projectId`)
5. `REACT_APP_STORAGE_BUCKET` (`storageBucket`)
6. `REACT_APP_MESSAGING_SENDER_ID` (`messagingSenderId`)
7. `REACT_APP_MEASUREMENT_ID` (`measurementId`)

#### Other `.env` Configurations

If you would like, you can add a `REACT_APP_SUPPORT_LINK` link to a form in which one may provide feedback on your college mapper application, in the form of a URL.

#### Subsequent Steps

1. `cd client`
2. `yarn && yarn start`

