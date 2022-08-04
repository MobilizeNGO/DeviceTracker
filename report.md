## MOBILIZE DEVICE TRACKER 

## ORGANIZATION NAME: Algoasylum (MOBILIZE)



---
---
## ACKNOWLEDGEMENTS
     
I am obliged to express my sincere regards to my team members, college faculty, and everyone who helped me during my internship.

It's my pleasure to give an appreciation and gratitude to the
organization's mentor Mr Shrirang Karandikar for his guidance and
proper direction at each step towards the completion of the internship.

I would also like to appreciate my college for giving me this opportunity.


Thanking You,

Akanksha Satpute

---------
----
## ABSTRACT

In this project, we put our efforts into building a real-time platform that can collect information about donors and recipients who may be located anywhere in the world. For that to happen we have used firebase's real-time database and Google cloud platform. Also by using the above technologies, we have tried to show the donors to whom we have donated their device and when we donated it.

It is very important to be transparent because donors may want to know where their devices are and they may want to know which recipient is using their device. This thing provides them
internal satisfaction and we as a part of the NGO will be
transparent from our end. For this to happen in real life we are
developing a platform for our NGO. This platform will have
different sections where donors and recipients can put their
information to be a part of the donation drive and donors will be
able to check where their devices are

---
---
## TABLE OF CONTENTS

ACKNOWLEDGEMENTS 

ABSTRACT

INTRODUCTION OF ORGANIZATION

- MOBILIZE

- MOBILIZE METHODOLOGY

MOTIVATION

PROBLEM STATEMENT

PROJECT OVERVIEW

WORK RESPONSIBILITY

CONCLUSION

REFERENCE

---
## People working in a team:-
-  Akanksha Satpute,
- Preeti Abnave

----
---
# MOTIVATION
We are building a platform for our NGO which will be helpful
for donation drives. The motivation for this task is that if someone
wants to donate a device then that person will be eager to see
where his donated device is and it is important from the donor’s
point of view to see where his donated device is. Working on this
project to provide such transparency to the donors motivated me
to build this platform.

---
---
## INTRODUCTION OF ORGANIZATION:-

## MOBILIZE
Mobilize is an organization working for NGOs which is started in 2021, with
a strong social motive. During the pandemic various crises took place, still, the
education system did not stop. Rather, it has been drastically changed with the
rapid rise of digital learning platforms. The online learning system has not yet
stopped even if there is no lockdown. Rather there is an increase in online learning
resources. Students can get knowledge about anything using a single click on their
machines but few students don’t even have a mobile for accessing these online
resources. To help such students who want to get knowledge from online resources,
Mobilize comes forward to help them by donating some devices like mobiles,
laptops, etc which will be donated from different donors.

## MOBILIZE METHODOLOGY
Mobilize procedure is to approach different people who want to donate
devices like phones, tablets, laptops, etc. After collecting such devices, Mobilize
checks for quality of such devices, separating these devices into working
conditioned devices and some may need to be repaired. Then, they would deliver
these devices to orphanages or students who need them. The actual donation is
working physically like someone will go and give that device to a particular needy
student but collecting the information of different donors and recipients is now
online using the mobilize platform we have developed.

----
---
## PROBLEM STATEMENT
Develop a platform that will help collect the data of different donors and
recipients who need devices like laptops, mobiles or tablets, etc. and
donors will be able to check whether their donated device has reached
needy students or not

----
---
## PLATFORM THAT WE HAVE USED
- ## FIREBASE:-
 For handling huge amounts of data and performing
different queries on the backend, firebase is a good platform. This
is used to handle real-time databases. Even if a website is hosted
on any platform, users can still enter data through the frontend and
that data will be reflected in the real-time firebase database.
Firebase Makes it easy to handle huge data in less time and cost.

- ## GCP - GOOGLE CLOUD PLATFORM:-
GCP is a cloud platform that provides various functionality
like hosting a website and creating a database for creating
databases it offers a MySQL database and this database can be
hosted on a MySQL server. It offers the functionality of storing
huge data on clouds instead of using any hard disk or hard drive
for storing this data.
People are using the Google cloud platform because it is easy to
use, reliable, more secure, and cost-effective as well.

- ## AUTHENTICATION:- 
People can log in to the website using an
email id and password but it’s a little hectic from the user’s point of
view so there is functionality in the cloud and firebase to log in
using Google Authentication and developers can use this
functionality for make user-friendly website or platform.

---
---
### WHAT FUNCTIONALITY DO WE USE FROM THE ABOVE PLATFORM AND HOW?

## FIREBASE:-
We have used firebase’s real-time database to handle data
that is continuously increasing like data of donors and
recipients growing and for handling such dynamic data
firebase’s real-time database is the correct choice so we
used it.

For actual implementation, we have created one firebase
project and in that project, we have created three different
database collections all three database collections have
different names like donors, recipients, and donation which
are used to handle data of donors, recipients, and donation
drive respectively.

## GOOGLE CLOUD PLATFORM (GCP):-
We have used GCP for hosting our platform and created one
bucket for storing all files required for the proper working of
our platform. We have to give all the required permissions to
the users and then we will be able to get a public link for our
platform. As we are hosting this platform on GCP, anyone
can visit our platform and use our interactive platform and
this platform will not only be restricted to admin.

## AUTHENTICATION:-
For user-friendly login on the platform we have used Google
Authentication which is provided by firebase and we have
hosted its coded file using GCP so that it will be runnable on
any machine.

----
----
## PROJECT ROLES:-
- This platform has various roles such as:
1. Individual Device Donors:-
Here individual people like you and me can visit mobilize
platforms and if we want, we may become a part of the
donation drive by donating some devices like mobile, laptops
or tablets, etc.

2. Device Recipients:-
These are the people who want devices only for educational
purposes. This may include school students, college
students, or any student willing to study.

3. Admin:- Admin is an owner of the platform, who has started
this social work. He can take a device from different people
and can donate these devices to specific needy people.


## BRIEF DESCRIPTION OF THE PROJECT:-
In this project, we are trying to create a platform having different
web pages for donors, recipients and one for admin use. All
these pages are connected to the backend with a real-time
firebase database and each page is connected to a different
collection of databases. For more description read the following:

For building a platform which is used to collect data of
donors and recipients , we have used HTML, CSS and Javascript
for the frontend part and for the backend we have used firebase's
real-time database.

In our first step, we were more concerned about the frontend so
we developed a frontend page for collecting donor’s information
using the above frontend technology and all the working of the
frontend is mostly based on the ids given to the data fields.

For collecting and storing the data from the frontend we
need some backend working on the backside. For that, we have
used firebase’s real-time database and in that, we have created
only one project where in the same project we have created three
collections for the donor’s database, recipient's database and one
for the page which is used for admin’s use. As we are working on
the firebase’s real-time database all the data is stored in the
key-value pair i.e in the JSON format.

When a user visits our platform, He will first see the frontend of
the platform and if he wants to register himself for the donation i.e
if he wants to register himself as a donor or recipient then he will
put the required data in the specific frontend page and click on the
submit button . We have added addEventListener on each submit
button which works for connection of frontend with backend. Each
addEventListner has a reference to the respective collection of
the database i.e addEventListner on the submit button of the
donor’s page has a reference to the donor's database collection.Like that, every button has a separate addEventListener to
connect it with the backend.

If a user puts the required data on the respective frontend
page and clicks on the submit button then the respective
addEventListner gets called and if the database collection is not
already created then that addEventListner will create a new
collection of the database else it will append data to the existing
database collection. For reading the data from the database we
have given the reference of the database collection and when we
click on the button of the read data function, the Onvalue function
will read each data from the database collection and append it to
the HTML table and this append operation is carried out based on
the id of the table.

In short, when we put the required data on the frontend of
the page and click on the submit button then the respective
function is called which we have used on the id of the submit
button and that function has a reference to the location of the
database collection of the required page. After we got that
location in the firebase real-time database, then data is going to
add to the database collection and the reverse thing is done for
the reading operation.

For reading the data from the backend , we have provided a
button on our frontend page and data will be displayed in the form
of a table. For this, we have created one table and provided it with
an id. When someone will click the read data button then the
respective function of reading data is getting called which will
have reference to the database location and using that reference
we have written one function where we are visiting each
document of the collection and fetching its data in one variable
and then we are appending that data to the table of specific id.
Like that we have created two more pages for recipients and one
for the admin use.

On the page of the donors, We have written one extra function for
checking to whom we have donated their devices . For that, we
have taken the reference of the database where we have stored
the information of whose device is donated to whom with their
email-id and when donor click on the track device button then we
are asking him the device-id of the donated device and based on
the device-id we are displaying him the recipient’s email id to
whom we donated his device. For proper working of the track
device function, we have written a function which will go through
the loop until gets a specific device-id. Once it gets a specific
device-id in the backend database then it will return the recipient’s
email-id to whom we donated his device.

- For code with proper setup and explanation visit to the
 https://github.com/MobilizeNGO/DeviceTracker/tree/main

 or
- https://docs.google.com/document/d/1XgzSsraxf9In2Ij5s8oXNCp5obASqYZzVxKwKsEyeW4/edit?usp=sharing

---
---

## CONCLUSION:-
During working on this project, I have explored many things like different cloud platforms. Through this exploration, I come to know what different types of services different cloud platforms are providing, and their pros and cons, and I come to know Google cloud is more secure, easy to use, reliable, and cost-effective as well so I have used Google cloud in the project. Also, I come to know how different services are working like MySQL is working well for a small amount of data and the server of MySQL is going down as the amount of data is going to increases that's why we used firebase real-time database which is used to handle huge amount of data efficiently.

By working on this project I got hands-on experience on how to work with the firebase database, how to enter data in firebase, and how to retrieve that data from the database. As we have developed all from scratch, I come to know how to code and make connections between the backend and the front by reading the documentation provided by Firebase.

This is my first experience of working with cloud and real-time firebase databases and this was a good experience and  this experience taught me many things like we should close each server after use otherwise we need to pay the unnecessary costs for using that server also the hands-on experience on how to connect frontend with backend, how to retrieve data from backend to frontend will be very helpful to me in my further journey when I will work on big projects of the industry.

---
---


## REFERENCES:- 
1. For reading and writing data in firebase
https://firebase.google.com/docs/database/web/read-and-write?hl=en&authuser=0

2. For Google authentication 
https://firebase.google.com/docs/auth/web/google-signin?hl=en&authuser=0

3. For Jquery/bootstrap link
https://firebase.google.com/docs/auth/web/google-signin?hl=en&authuser=0




