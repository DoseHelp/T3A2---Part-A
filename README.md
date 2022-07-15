# Eman Youssef and Calvin Dexter - T3A2 Part A
## DoseHelp: Full-Stack App Assignment
---
### Purpose
We want to develop this to replace and improve the Opioid Treatment Program's current system which is for the Pharmacy to manually check on patients, whereas this is a solution for the Pharmacy to keep track of Opioid Treatment Program patient's payments and dosages online instead of manually. The current system is used to check on a patient by getting their prescription and checking if it’s in date. Then go through the OTP’s files (that are on paper) to find them by name and add the dose and payment to that paperwork.

### Target Audience
The App will be aimed at Pharmacists to use as a tool to make their job easier as the practices currently being used are outdated and tedious. DoseHelp will be a solution for the Pharmacist to use when catering to OTP patient making for a more efficient workload for a busy Pharmacy as doses for the program are used daily. 

### Functionality / Features 
The app will have three types of users: Guests, Pharmacists and Admin. A Guest must have an admin create an account before gaining access to the main features of the application. 

Once the Pharmacist is an authenticated user, they will be able to add a new Patient or edit/delete a current patient.

Within a Patient’s details, there will be a list of past doses relevant to them and the ability to add a new dose to that patient. It also displays if the patient has a credit or not. 

Adding a new dose for a patient will take the information including the Prescription, Drug and 
Payment. If the patient specifies they want to use their credit for the payment, then it will take away the amount specified from their existing credit. 

A dose’s details will have the ability to update and delete its information.

#### Admin
- Create account 
#### Guest 
- Login
#### User 
- Logout 
- Add/edit and delete patient 
- Add/edit and delete dose details

#### App tracks a Patients dose
- Prescriptions
- Drugs
- Payments
- Doctor
- Pharmacist
#### The diagram shows how these main entities relate to each other
![Entite Diagram](/docs/Entities/EntitieExample.png)

The doctor writes a prescription and sends it to the pharmacy. A pharmacist enters the details of the prescription into the system. When a patient comes to the pharmacy, a pharmacist then starts a dispensing process.
Dispensing process: the drug is simply supplied to a patient after all the details of the patient, doctor, drug, prescription and pharmacist are entered into the system and checked by the pharmacist. The pharmacist then enters the credentials and updates the dispensing details.

![Dispensing Process](/docs/Entities/DispensingProcess.png)
---
### Data flow Diagram
The data flow diagram represents the flow of data through the DoseHelp system. The system consists of five main modules:

1- Signup / Login Process: 
**Where data is coming from: **Signing up will require information from the pharmacist like Username, email and password as well as authorization from the administrator who will have access to the “add new user” functionality.
**Where data is going and how it is being stored:** That information will be sent to the user database to be stored and used in the verification and authentication process while logging into the system.

2- Managing Patient records: 
**Where data is coming from:** The system will keep track of patients' information through an authorised pharmacist who can add, update or delete patients.
**Where data is going and how it is being stored:** the data will be stored in the database in a patient table for later use in dispensing and reporting functionality. 

3- Managing Prescriptions: 
**Where data is coming from:** Prescriptions coming into the pharmacy for Opioid patients will be recorded by an authorised pharmacist.
**Where data is going and how it is being stored:** the data will then be stored in the database in the prescription table to be used later in the dispensing process.

4- Managing Drugs Information: 
**Where data is coming from: **Drugs details used in the Opioid program will be recorded by an authorised user.
**Where data is going and how it is being stored:** The data will be stored in the database in the Drug table and will be used in the dispensing process.

5- Managing Dispensing and Payments: 
**Where data is coming from**: In this process, the pharmacist will search for a certain patient given his name and date of birth and the system will retrieve the patient's details and the prescriptions related to that patient along with the drugs prescribed and the payments made. 

**Where data is going and how it is being stored:** The data will then be stored in the dispensing table with all the changes made by the pharmacist after dispensing and receiving payments if any.
![Dataflow](/docs/Dataflow/Dataflow.png)

### Architecture Diagram

![Architecture Diagram](/docs/ArchitectureDiagram/ArchitectureDiagram.png)

### User Stories

| As a: | Action | Reason |
| ------ | ----------- | ----------- |
| Pharmacist | I want to be able to login on to the system | So that all the transactions I do on the system would have my credentials and time stamp on them. |
| Pharmacist | I want to be able to add/edit the patients data. | So that I would be able to add a patient to the system or edit their details. |
| Pharmacist | I want to be able to enter/edit prescription details. | So that I would be able to retrieve the details later on. |
| Pharmacist | I want to be able to edit medication details. | So that I would be able to edit medication details if the manufacturer change its form or quantity. |
| Pharmacist | I want to be able to check patient credit status. | So that I would decide to ask for payment or not. |
| Pharmacist | I want to be able to retrieve patient prescriptions. | So that I would be able to dispense the medication. |
| Pharmacist | I want to be able to enter my credentials before dispensing | So that the system will keep track of who dispenses the drug and when. |
| Pharmacist | I want to be able to create reports of the patient | So that I can see how many times the user missed a dose. |
| Admin | I want to be able to create a user | So that the user can use the system. |
| Admin | I want to be able to do everything a Pharmacist can do | So I can have access to all the information and features of the system. |

---

### Wireframes

![Signing In](/docs/Wireframes/Signingin.png)
![Landing Page](/docs/Wireframes/LandingPage.png)
![Patient Page](/docs/Wireframes/PatientPage.png)
![Patient Details Page](/docs/Wireframes/PatientDetailsPage.png)
![New Patient Page](/docs/Wireframes/NewPatientPage.png)
![Notes Page](/docs/Wireframes/NotesPage.png)
![Prescription Page](/docs/Wireframes/PrescriptionPage.png)
![Medication Page](/docs/Wireframes/MedicationPage.png)
![Doctors Page](/docs/Wireframes/DoctorsPage.png)
![Dispensing Page](/docs/Wireframes/DispensingPage.png)
![Reports](/docs/Wireframes/Reports.png)
![Help Page](/docs/Wireframes/HelpPage.png)
![Users Page](/docs/Wireframes/UsersPage.png)

### Workflow

#### Sprint Plan:

Building the Application, we have divided the workload into five parts and will try to finish as much as we can before moving on to the next sprint. We will add an urgency level to each task on our Trello board and add new tasks as they arise. 

If we have a backlog of tasks from things we may have missed in the last sprint we have some dedicated time to work through the backlog of tasks.

- Sprint 1: Set up Back-end with rails and RSpec, test CRUD with Postman
- Sprint 2: Set up Front-end with React and add components
- Sprint 3: Login Authentication
- Sprint 4: Work through React components and deploy both ends
- Sprint 5: Styling and finalising sprints backlogs

#### Trello Screenshots

- __[Link to Trello board](https://trello.com/b/f8mwuGKb/dosehelp)__ 

![Home](/docs/Workflow/Home.png)
![Dataflow](/docs/Workflow/Data.png)
![User Stoires](/docs/Workflow/User.png)
![Wireframes](/docs/Workflow/Wireframes.png)
![Activity](/docs/Workflow/Activity.png)

### Tech Stack

- **Front-end:** REACT.js, Javascript, JSX, HTML,bootstrap and CSS

- **Back-end:** Ruby On Rails

- **Database:**  PostgreSQL

- **Testing:** Spec, Postman

- **Deployment:** Back-end: Heroku, Front-end: Netlify

- **Management:** Discord, Trello, GitHub