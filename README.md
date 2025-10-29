you can select an sender in your gmail from whom you want to delete all emails. 


# Steps

## 1. virtual environment and downloading libraries

### to start a venv (so you can download libraries without actually downloading them onto ur computer):     
    python -m venv .venv
    (run this every time you want to run gmaildeleter)
    source .venv/bin/activate 

### downloading
    npm install http-server

## 2. get Client ID

from javascript quickstart (https://developers.google.com/workspace/gmail/api/quickstart/js), follow the same steps:

"
### Set up your environment


#### **Enable the API**

Before using Google APIs, you need to turn them on in a Google Cloud project. 

In the Google Cloud console, enable the Gmail API (https://console.cloud.google.com/flows/enableapi?apiid=gmail.googleapis.com)

#### **Configure the OAuth consent screen**

In the Google Cloud console, go to Menu menu > Google Auth platform > Branding (https://console.cloud.google.com/auth/branding).
Create a new project if need be.

#### **If you see a message that says Google Auth platform not configured yet, click Get Started:**

Under App Information, in App name, enter a name for the app.

In User support email, choose a support email address where users can contact you if they have questions about their consent.

Click Next.

Under Audience, select either.

Click Next.

Under Contact Information, enter an Email address where you can be notified about any changes to your project.

Click Next.

Under Finish, review the Google API Services User Data Policy and if you agree, select I agree to the Google API Services: User Data Policy.

Click Continue.

Click Create.


#### **Authorize credentials for a web application**

To authenticate end users and access user data in your app, you need to create one or more OAuth 2.0 Client IDs. A client ID is used to identify a single app to Google's OAuth servers. 

In the Google Cloud console, go to Menu menu > Google Auth platform > Clients (https://console.cloud.google.com/auth/clients)

Click Create Client.

Click Application type > Web application.

In the Name field, type a name for the credential. This name is only shown in the Google Cloud console.


#### **Add authorized URIs related to your app:**

Authorized JavaScript Origins:

    http://localhost:8000
    
Authorized redirect URIs:

    http://localhost:8000/auth/google/callback

Click create. Note the Client ID that pops up.

### **_Copy it then add it to the code (line 29) where it says 'YOUR_CLIENT_ID'._**


#### **Add yourself as allowed user**

Go to Audience in the tabs on the left.
Add your email of choice (that you want to delete) as a test user. 
Feel free to add more emails that you want to delete emails from, as long as you can log into them.
Click save
#### **Add Scopes**
Go to Data Access in the tabs on the left.
Click add or remove scopes.
Select the first link scope that pops up when you filter by each of these keywords: 
    labels
    modify
    mail.google
Click update then save.

## 3. **Create an API key**

In the Google Cloud console, go to Menu menu > APIs & Services > Credentials (https://console.cloud.google.com/apis/credentials).

Click Create credentials > API key > Create.

Your new API key is displayed.

### **_Copy it then add it to the code (line 30) where it says 'YOUR_API_KEY'_**



## 4. **Run the sample**

In your working directory, start the web server:

    npx http-server -p 8000
    
In your browser, navigate to http://localhost:8000

#### **Your first time running it, it'll ask you to continue (or go back to safety lol, press continue) and then approve scopes -- Do so.**
