
# Connect a secure Cloudant database instance to your web application


IBM Cloudant is a fully managed JSON document database that offers independent serverless scaling of provisioned throughput capacity and storage. Cloudant is compatible with Apache CouchDB and accessible through a simple to use HTTPS API for web, mobile, and IoT applications.

In this workshop you will learn how to connect your IBM Cloudant instance with your application. 


## Prerequisites

- [IBM Cloud Account](http://ibm.biz/jtcloud)

- Node package manager installed in your PC (https://nodejs.org/en/)

## Step 1: Sign-up/Login to IBM Cloud

1.1- If you are an existing user, click on this link to Login:http://ibm.biz/jtcloud

And if you are not, don't worry! We have got you covered! There are 3 steps to create your account on IBM Cloud: 

1.2- Put your email and password. 

1.3- You get a verification link with the registered email to verify your account. 

1.4- Fill the personal information fields. 

** Please make sure you select the country you are in when asked at any step of the registration process.

![image](https://user-images.githubusercontent.com/16270682/140926329-d798e427-5b56-4b6c-bfe7-aacf4543b24c.png)

## Step 2: Download Sample code

Download the sample app From workshop's [Git Repository](https://github.com/jstevenperry/IBM-Developer.git) click on code and download zip file. Unzip the file to a path of your choice.







## Step 3: Create an instance of Cloudant

3.1 - Fron Dashboard search for Cloudant service in catalog and select

<img width="619" alt="1" src="https://user-images.githubusercontent.com/16270682/143212659-c30bc3b8-9625-4e7a-839d-97e7c9427fb1.PNG">


3.2 - Click on create. You will be re-directed to your IBM Cloud Dashboard, select Cloudant from resource list.

<img width="919" alt="2" src="https://user-images.githubusercontent.com/16270682/143212674-f1d7d191-1cbe-4ed6-94ed-a75f8b19a89d.PNG">



## Step 4: Create Credentials 


4.1 - We will need credentials in order to connect Cloudant service with our sample app. To create credentials, from Cloudant service window, select Service credentials from the left menu. Click the New credential (+) button


<img width="935" alt="3" src="https://user-images.githubusercontent.com/16270682/143214356-7acaa032-2189-4924-88e0-218439d14f12.PNG">


4.2 - Give a name for your credentials and click on add 

<img width="634" alt="4" src="https://user-images.githubusercontent.com/16270682/143214509-04a025ac-97c3-48f5-962c-1f34cd1f0856.PNG">


## Step 5: Create Database

5.1 - Go to manage, Click on Launch Dashboard

<img width="941" alt="6" src="https://user-images.githubusercontent.com/16270682/143218403-7631b2f7-63df-44be-8917-69c0ac91d57e.PNG">

5.2 - From Cloudant Dashboard select, create database, name your database "**shopping_list**", click create

<img width="947" alt="7" src="https://user-images.githubusercontent.com/16270682/143218590-0d1441a1-5f8a-4db0-9d64-6d51f6cba505.PNG">

5.3 - Notice that right now your database is empty

<img width="898" alt="9" src="https://user-images.githubusercontent.com/16270682/143225087-7d0464f4-18c4-46bd-851a-4f2de95ad699.PNG">


## Step 6: Create service credentials config file 



6.1 - Open your sample app in your editor (mine is Atom), create a new file, paste in the below code and save it as :"**vcap-local.json**" in config directory.


    {

      "services": {

      "cloudantNoSQLDB": {

      "credentials":

      PASTE CREDENTIAL INFO HERE

      ,

      "label": "cloudantNoSQLDB"

      }

        }

        }



<img width="787" alt="8" src="https://user-images.githubusercontent.com/16270682/143224577-81bc2ec4-10b2-4ec2-ad4f-a49164d1ce8f.PNG">


6.2 - From Cloudant service window (where you created your credenttials in step 4), copy credentials 



<img width="741" alt="5" src="https://user-images.githubusercontent.com/16270682/143225179-fd6c338b-9391-4e87-aedf-351214ee5997.PNG">


6.3 - In vcap-local.json, replace the "**PASTE CREDENTIAL INFO HERE"** with the credentials you’ve just copied.

<img width="943" alt="10" src="https://user-images.githubusercontent.com/16270682/143225857-5a2c920b-54e3-4981-91b9-8a77fd43fe4a.PNG">


## Step 7: Load application data into Cloudant Database

7.1 - To load data in your Cloundant database run the following commands 

      npm install

      npm run load-db

## Workshop Resources


Login/Sign Up for IBM Cloud: http://ibm.biz/jtcloud

Workshop Replay: https://www.crowdcast.io/e/journeytocloud1

## Done with the workshop? Here are some things you can try further

- [Extract data from XML and expose it as a service](https://developer.ibm.com/tutorials/convert-xml-to-data-as-a-servicedaas-using-cloudant-nosql-database/?mhsrc=ibmsearch_a&mhq=Cloudant)

- [Get started with Node.js](https://developer.ibm.com/gettingstarted/node-js/)


## Links to the next sessions in "Journey to Cloud"

### 29th November- 6PM-8PM (GMT+4) 

- Deploy a Python-Flask application on IBM Cloud

- https://www.crowdcast.io/e/journeytocloud2

### 2nd December- 6PM-8PM (GMT+4) 

- Monitor and Secure your Flask application on the Cloud

- https://www.crowdcast.io/e/journeytocloud3

### 6th December- 6PM-8PM (GMT+4) 

- Create a Credit Analysis classification model with little to no code.

- https://www.crowdcast.io/e/journeytocloud4


### 8th December- 6PM-8PM (GMT+4) 

- Predict your insurance premium cost from your web application.

- https://www.crowdcast.io/e/journeytocloud5
