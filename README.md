# Backend-Test-Hospital-API

https://pacific-ridge-92098.herokuapp.com/
https://hospitalapibackend.herokuapp.com/
Hospital-API
I have design an API using Node.js and MongoDB for the doctors of a Hospital which has been allocated by the govt for testing and quarantine + well being of COVID-19 patients.

Features
There can be 2 types of Users

Doctors & Patients
Doctors can log in
Each time a patient visits, the doctor will follow 2 steps:
Register the patient in the app (using phone number, if the patient already exists, just return the patient info in the API)
After the checkup, create a Report.
Patient Report will have the following fields
Created by doctor
Status: Can be either of: [0 :Negative, 1:Travelled-Quarantine, 2:Symptoms-Quarantine, 3:Positive-Admit]
Date

Install dependencies

  npm install
  
  Run following command:

npm install bcrypt
npm install express
npm install jsonwebtoken
npm install mongoose
npm install passport
npm install passport-jwt
  
Start the server

  npm start
Documentation
Root Hosted Link - https://pacific-ridge-92098.herokuapp.com/
https://hospitalapibackend.herokuapp.com/
Routes :

a. /doctors/register - Registers a new Doctor.
b. /doctors/login - Authenticates and returns the JWT token to be used.
c. /patients/register - Allows a doctor to register a new patient (JWT Auth enabled).
d. /patients/:id/create_report - Allows a doctor to create a patients report (JWT Auth enabled).
e. /patients/:id/all_reports - Sends all the reports of a patient oldest to latest. (JWT Auth enabled).
f. /reports/:status - List of all the reports of all patients with a specific status. (JWT Auth enabled).
Data that needs to be sent with a route :

a. /doctors/register - name, email, password (Form type data)
b. /doctors/login - email, password (Form type data).
c. /patients/register - JWT Token (In Headers), name, phone, age, sex, comorbidity status (Form type data).
d. /patients/:id/create_report - JWT Token (In Headers), Patient's ID (params), status (Form type data).
e. /patients/:id/all_reports - JWT Token (In Headers), Patient's ID (params).
f. /reports/:status - JWT Token (In Headers), status (params).
Folder Structure

a. index.js - Server runs here
b. models - Contains all the models for Doctor, Patient, Report.
c. routes - Contains all the routes.
d. controllers - Contains all the controllers.
e. config - Contains all the config files.
