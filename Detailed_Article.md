# Device Tracking Mechanism

## Abstract 
Through this project we are trying to solve a problem which states that donors who are donating their devices need to get a confirmation where their devices are donated for this purpose, it's very important to provide a solution for this problem. Donors must be able to track the devices and should be able to know the recipients.

Now this seems interesting because there should not occur any type of misconception of their devices like where they got donated or any type of false assurance to device donors as they have donated for a good cause. A good proof that they can view by themself and track will resolve all their doubts.

The solution which we tried to achieve is conveyed in detail through this article. Our solution will make the donor enable to donate the device through interface and can track it as well. 

---

## Acknowledgements 
I am obliged to express my sincere regards to my group members and everyone who helped me during my internship.

It's my pleasure to give an appreciation and gratitude to the company mentor Mr. Shrirang Karandikar for their guidance and proper direction at each step towards the completion of internship. 

I would also like to appreciate my college for giving me this opportunity.



Thanking You,

Preeti Abnave

---
## Table of contents

ABSTRACT<br>
ACKNOWLEDGEMENTS<br>
INTRODUCTION<br>
MOTIVATION
1. INTRODUCTION OF ORGANIZATION                                       
    1.1 MOBILIZE<br>
    1.2 MOBILIZE METHODOLOGY<br>
2. ARCHITECTURE<br>
3. PROBLEM STATEMENT<br>
4. PROJECT REQUIREMENTS<br>
    4.1 USERS ROLES<br>
    4.2 FUNCTIONALITIES<br>
5. WORK RESPONSIBILITIES<br>
6. DETAILED WORK<br>
    6.1 GCP<br>
        6.1.1 PROJECT CREATION<br>
        6.1.2 IAM USERS<br>
        6.1.3 CLOUD STORAGE<br>
    6.2 FIREBASE<br>
        6.2.1 REAL-TIME DATABASE<br>
    6.3 DEVICE DONORS<br>
    6.4 RECIPIENTS<br>
    6.5 MOBILIZE ADMIN<br>
    6.6 AUTHENTICATION <br>
7. CONCLUSION & FUTURE SCOPE

---
## Introduction

Consider a person (donor) who has many devices, some are in good condition, some are not, some need to be repaired, etc. Now, if the person  (donor) thinks that, let's throw it away and buy a new one, which seems extremely fine. Also, the person might think in a way that lets them sell on OLX or exchange through Amazon which again seems perfectly fine. But how about donating these devices for a good cause?, so that these old phones or laptops can be used by someone who needs it. But again a question occurred: what about the guarantee of the devices donated exactly to the person (students) who needs it. 

For this, we have tried to develop a solution with the help of which the person (donor) will be able to trace the devices which are donated. In this solution we have used google cloud platform and firebase as an interactive technology and JavaScript to connect firebase and gcp. Also we have used Firebase Authentication feature so that the security is maintained. The further article will elaborate the solution.

---
## Motivation
The motive of the project is to trace the devices, which will get donated by the donors, so that the device donor will get assurance of their donation and there will be transparency between the donor and their donated devices. Here the aim is that the donor should know their devices to whom it was donated and details of the receivers.

---
## 1. Introduction to Organization

### 1.1 Mobilize

Mobilize is an NGO which started in 2021, with a strong social motive. Now-a-days education system has advanced its way of learning. Students have multiple options to gain education. But still some of the students don't get the resources, so the awareness, interaction to handle new technologies is not reachable to them. During the covid-wave, distance-learning became one of the good options for students without omitting their studies. Rather, it drastically changed with a rapid rise of digital learning platforms. But there was still a problem of resources like laptops, phones, tablets, etc, which a middle class or underprivileged student wouldn't have afford. Mobilize came with a solution to this problem, and decided to be a helping hand to children who need such devices for their education. The aim is also to extend the help beyond pandemic because some students cannot access the resources while others take it for granted.  

### 1.2 Mobilize Methodology 

Mobilize procedure was to approach the people or corporates who wanted to donate devices like phones, tablets, laptops, etc. After collecting such devices, mobilize then checks for quality of such devices, separating devices into working conditioned devices and some may need to be repaired. Then, they would deliver the devices to orphanages or students who need them. This method was followed through drives.

---
## 2. Architecture

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/architecture.png)

The above architecture gives us a glimpse of  how the solution must be structured. We see the mobilize website where donors, receivers and mobilize admin interface is designed. Here the interface is the form in which they will see onces they authenticate themselves through google sign-in method which is the authentication feature of firebase. Nextly the which person has what all rights like to track or display the data is clearly reflected through the architecture. Here the data transfer takes place from gcp to firebase and visa-versa with the help of API and SDK’s.

---
## 3. Problem Statement

Developing a mechanism through which the device donors can track a device and be able to get answers to questions like who donated what? Donated to whom? and Where it was donated?. A provision that the donor should be able to view the details of the recipients

---
## 4. Project Requirements

### 4.1 User Roles
This platform has various roles while interacting with the platform such as: 

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/roles.png)

### 4.2 Functionalities

These roles has some specific task/functionality which they have to  perform such as:

- **Device donors**
  
    The device donor can submit their information and the device description.

    The device donor can track their donated devices.

- **Device Recipients** 
  
    The device recipients can submit requests for any particular desired device. 

- **Mobilize Admin** 
    
    The mobilize admin can assign the device to respective recipients by  device ID as per their demand.

    They can view all information of donors.

    They can view all information of recipients.

    They can track their donated devices.

---
## 5. Work Responsibilities
My task in mobilize was in the backend domain. It was developing the mechanism so that the data collected from the user interface should be able to get stored and sync in real-time in an unstructured way as well as building a connection so that handling the data becomes easier.  

---
## 6. Detailed Work

Before actual implementation, it was important to decide which technologies to use. Now-a-days new start-ups or NGO’s try to provide their services through cloud, as maximum features are available and there is no need to build from scratch. A ready made infrastructure and security responsibilities are taken care of by cloud providers itself. Also, various choices for choosing cloud services are provided. Following are the technologies used for developing the solution.

### 6.1 GCP - Google Cloud Platform

Google cloud platform provides cloud computing services, where users need not have physical machines. 
Google cloud console, which is a dashboard provides  an interface to manage all the resources and projects.

### 6.1.1 Project Creations

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/project%20creation.jpg)

Firstly we created a project under Mobilize. A unique project number and project ID was assigned by the cloud provider or we can set our own ID as well which should be a numeric string. A project ID helps to differentiate projects from the rest of all created on console.

### 6.1.2 IAM Users

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/rule.JPG)

As there are different tasks which need to be carried out by project team members. We used google cloud IAM service which helped us to get access to different resources so that simultaneously we can work on the project. Various roles such as Editor, Viewer, Owner, Admin, etc. options are available for different services. This helps to organize roles and responsibilities to team members. Preventing access to confidential data helps to be secure data and helps any modifications. Multiple roles can be assigned to a particular user. Like my role was owner for a project and viewer for some services like the billing section.

### 6.1.3 Cloud Storage

We used cloud storage for storing all the objects like files of any formats. All the files are stored in the container called a bucket under a mobilize project.

For our project, we have 
**Auth HTML** file where code for authentication is programmed using script tag **Auth CSS** file is imported into it. 

Nextly, **Donor HTML** file will be displayed for the donor so that he could be able to enter the details and can view other functionalities as well.

**Recipient HTML** file which will display for the recipient so that he could request for a device.

The **Donation HTML** file consists of all the functionalities. And only the mobilized admin can view the file.

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/storage.JPG)

After uploading the files onto the bucket. We can access it through the browser using google storage apis. For that, going to the permission tab and then allowing the public access will provide us with urls to access any particular web page.

---
## 6.2 Firebase

The main configuration in Google Firebase we performed is building connection to frontend and to obtain the real-time data. This was obtained with the help of the firebase SDK and API which is mentioned below.

**Firebase SDK setup and configuration:**

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/fire.jpg)


- **Content Delivery Network:** Using the CDN script helped to connect firebase to cloud as fast as possible. So that the data in the firebase database will get quickly deployed on the user interface.
  
- In the script tag the **type = module** enables firebase modular bundlers to manage various imported libraries and to reduce the SDK size. SDK size means the software development kit size which helps to build a custom web app, add some add-ons and to connect to any other program.
  
- Nextly the mobilized web app was initialized into firebase by the statements **import { initializeApp } from "firebase/app".**

- In **firebaseConfig constant** declared ID’s are the ID’s assigned while creating the web app. This **API key** will help to call certain API’s, **Application Id** defines in firebase which platform to use like web, **Project Id** will help to identify the project over the firebase and google cloud.

### 6.2.1 Real-Time Database

The Firebase Realtime Database is a cloud-hosted NoSQL database that lets us store and sync data between our users in real-time. The following is the way through which we configure the rules which will enable the firebase database to store data.

**Step1:** Before using a realtime database we have to edit the rules. 

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/firerule.png)

Here rules are defined as read or write. So if we want to write to the database to store data then it should be set to true. If we want to read the data from the firebase database then we should set the read value as true. The above rules are set for the data to get stored into firebase. This rule is defined in JSON format in a key-value pair. Also, these are some of the build-in firebase security configuration that one can set as per our needs.

**Step2:** Viewing the stored data.

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/real.JPG)

We can see the url which gets created through which the data gets stored in firebase. Here the name of the database is newform. Below it are the random keys created for each record when we entered. The attributes/keys with its values are shown in string format. This is again stored in JSON format by the firebase. 

---
## 6.3 Device Donors

[This is the GitHub Link for HTML codes](https://github.com/MobilizeNGO/DeviceTracker.git)

Device Donor is one of the roles of the user, then it can be an individual donor who wants to donate their old phones, laptops, tablets, etc. Can communicate from the below given snapshot and can provide their information.

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/donor.png)

A form is created in html with div, labels and input tags. The **form attributes ids => first-name,  last-name, email, deviceid, devicedesc** which are very important unique ids for HTML elements. With the help of which the values are accessed through frontend form and at the backend they are stored in variables.

**According to the Functionalities there are 2 buttons:**
- Donate Button
- Track My Device

**Triggering the Donate Button, the following procedure will take place:**

- The connection between the submit button and the function is by id which is **donate** => id of Donate Button.

- AddEventListener() method will help to trigger the  Donate Button when it is clicked. So that the statements will get executed.

- With the help of ids given to elements the data first is accessed by variables declared by using the **var** keyword. The ids are called by **document.getElementById()** method.

- Nextly, an **if statement** is defined with the help of which validation takes place. The **alert()** will display a pop-up saying that the text-box is empty and some value needs to be provided if it is NULL.

- After accessing the data in variables they are pushed onto the database using the **push()**. Here **ref()** will direct to the database of firebase in this case it is **donors**.

- Setting the accepted data from a variable in the database using **set()**. In the database it will be stored in JSON format.

**This is how the data get stored in Firebase Real-time database for donor:**

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/donorreal.JPG)

The data gets stored in JSON format in key-value pairs. The above data is unstructured. But the donor needs to provide all the information as validation is provided to the form.
 
---

**FLOW-DIAGRAM TO SUBMIT DATA:**

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/flow1.png)	

---
## 6.4 Recipients
Recipients are one of the roles of the user, who are in need of the devices. Students need devices for elearning so that they can understand better by watching youtube, using Khan Academy. Also can complete various online courses. They can communicate from the below web page and can provide their information: 

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/rec.png)

A form is created in html with div, labels and input tags. The **form attributes ids => first-name,  last-name, email, devicedesc** which are very important unique ids for HTML elements. With the help of which the values are accessed through frontend form and at the backend they are stored in variables.

**According to the Functionalities the following is the button:**
- Make a Request

**Triggering Make a Request button the following procedure will take place:**

- The connection between the submit button and the function is by id which is **request** => id of Make a Request Button.

- The code works similar to the Donate button.

- After accessing the data in variables they are pushed onto the database using the **push()**. Here **ref()** will direct to the database of firebase in this case it is the **recipient**.

**This is how the data get stored in Firebase Real-time database for receiver:**

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/recreal.JPG)

---
## 6.5 Mobilize Admin

Mobilize admin is one of the roles of the mobilize authority who can view all the details. Mobilize admin needs to connect the device donor to the recipients by assigning the devices which recipient needs through the device ID which is unique for all devices. The following is the information which the mobilize admin can view and add.

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/mob.png)

An admin form is created in html with tags. The **form attributes ids =>emaild,  emailr, devid** which are unique ids for mobilize admin form input tags. 

**According to the functionalities the following are the buttons:**
- Connect
- All Device Connections
- All Donors
- All Recipients
- Track Devices
 
**Triggering Connect button the following procedure will take place:**
 
- The connection between the submit button and the function is by id which is **connect** => id of Connect Button.

- This works similar to previous Donate and Make a Request button.

- After accessing the data in variables they are pushed onto the database using the **push()**. Here **ref()** will direct to the database of firebase in this case it is **donation**.

**Triggering All Device Connections,  All Donors, All Recipients buttons the following procedure will take place:**

- The connection between the **All Device Connections,  All Donors, All Recipients** button and the function is by ids which is **getConnect** => id of All Device Connections button, **getDonor** => id of All Donors button, **getRec** => id of All Recipients button.

- Tables ids for the same above mentioned buttons are **dataTb0, dataTb1, dataTb2** with the help of which the data will appear in respective tables.

- The **remove()** will clear all the previously displayed data each time when the button is triggered.

- **Var rowNum** is declared to have a proper index or serial number when displaying the data.

- Firstly, we define **dbRef** constant which will have the data from the database donation by using **ref()** method.

- Secondly, the **onValue()** is defined to read the path and listen for changes. Here the path is dbRef and the snapshot means to read the data from the path.

- Now the **forEach** childSnapshot will iterate through each record from the database. The **childSnapshot.key** and **childSnapshot.val()** is called which will call the random string which is key like **“-N7lI5-bzla3k0TGV8ZD”** and the val() will get the entire data under that particular key. 

- These values and keys are stored in constant **childKey** and **childData**. Which further helps to get each value in tables through constant and the ids like **childData.emaild.**

- Lastly, these rows are appended into the table which is called by respective ids.

---
**FLOW-DIAGRAM TO VIEW DATA:**

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/flow2.png)

---

## 6.6 Authentication
In our project we use firebase authentication using google sign-in method following are the steps required to set up the authentication configuration.

**Step1:** We select mobilize as our project. Firebase drive to authentication page after selection. After selecting the sign-in method tab we get numerous sign-in options.

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/auth.JPG)

We chose Google authentication as a sign-in method and then a unique id got generated for authentication and it asked for a sample gmail to sign.

**Step2:** As we are trying to sign-in from the frontend which is hosted on cloud storage. In firebase there is an option of Add Domain. Where we need to provide the domain of the platform where we are hosting the authentication page. 

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/domain.JPG)

In the above snapshot, there are some of the default domains set by firebase which are to connect the localhost, firebase app and firebase web app. We added the storage.googleapis.com domain where we have hosted the authentication page.

**Step3:**  Sign-in quota

![](https://github.com/MobilizeNGO/DeviceTracker/blob/main/images/signin.JPG)

Manually setting the sign-up quotas so that anonymous accounts are restricted. Maximum sign-ups per hour we eat as 100. Also dates are set so that beyond that particular date the user will not be able to sign-in. 

**Step4:** Signing-in from the front end. 

We can view all the users who are signed-up in firebase through navigating to **Users tabs**. Information like user gmail as an identifier, provider like google, when did the user create an account the date and when did user sign-in get stored in firebase. As well as a unique ID while creating the account.  

---

## 7. Conclusion & Future Scope
During the solution development, Firstly we tried to structure the requirements needed to develop the solution. Like a form which will help to collect the information from the donor then a form for a receiver to make a request. Secondly, a provision for the mobilize admin to assign the devices to receivers. Nextly, the assigned devices of a respective donor were able to be viewed at the donor's end. For the security purpose we tried to carry out firebase authentication so that the donor, receiver and admin can authenticate themselves and their information is stored in the database. Step-by-step adding the functionalities helped to obtain a uniform solution.

This experience helped me to explore GCP and its features. I could understand the use of the GCP account billing system and its service prices. Firebase as a backend, provided an infrastructure which is easier to understand. As it provides various services for web, app and analytics. Building connection from firebase to cloud through firebase SDK and API enables the operations like view, modify, access and store the data smoothly. Before implementing a piece of code a thorough research helped to solve the errors. Google cloud documentation acts as a guide to reach a desired solution.
  
When I saw the developed solution, now I felt it's important to gain a strong hands-on knowledge on JavaScript. I understood that never use any GCP or firebase services without doing a cost comparison.  

This solution can be improved by setting up a mechanism of how long the devices are in use by the recipients. Some more queries which will give some statistical analysis like how many recipients and donors have registered. In total how many devices are present, how many are allocated to receivers. 

---
*Submitted by*
#### Preeti Abnave  
#### MKSSS’s Cummins College of Engineering for Women, Pune.
#### For organization: MOBILIZE
#### Team Members : Preeti Abnave & Akansha Satpute









