you can select an sender in your gmail from whom you want to delete all emails. 



to start a venv (so you can download libraries without actually downloading them onto ur computer):     
python -m venv .venv
source .venv/bin/activate (run this every time you want to run gmaildeleter)

npm install http-server

change the API key and the client ID to whatever yours is, details on how to get to them incoming.

create .env file:

    const CLIENT_ID = 'YOUR_CLIENT_ID';
    const API_KEY = 'YOUR_API_KEY';

from javascript quickstart (https://developers.google.com/workspace/gmail/api/quickstart/js), follow the same steps:

"**Set up your environment**

To complete this quickstart, set up your environment.

**Enable the API**

Before using Google APIs, you need to turn them on in a Google Cloud project. You can turn on one or more APIs in a single Google Cloud project.
In the Google Cloud console, enable the Gmail API.
https://console.cloud.google.com/flows/enableapi?apiid=gmail.googleapis.com

**Configure the OAuth consent screen**

If you're using a new Google Cloud project to complete this quickstart, configure the OAuth consent screen. If you've already completed this step for your Cloud project, skip to the next section.

In the Google Cloud console, go to Menu menu > Google Auth platform > Branding.
https://console.cloud.google.com/auth/branding

If you have already configured the Google Auth platform, you can configure the following OAuth Consent Screen settings in Branding, Audience, and Data Access. If you see a message that says Google Auth platform not configured yet, click Get Started:
Under App Information, in App name, enter a name for the app.
In User support email, choose a support email address where users can contact you if they have questions about their consent.
Click Next.
Under Audience, select Internal.
Click Next.
Under Contact Information, enter an Email address where you can be notified about any changes to your project.
Click Next.
Under Finish, review the Google API Services User Data Policy and if you agree, select I agree to the Google API Services: User Data Policy.
Click Continue.
Click Create.
Add the scope: .../auth/youtube

**Authorize credentials for a web application**

To authenticate end users and access user data in your app, you need to create one or more OAuth 2.0 Client IDs. A client ID is used to identify a single app to Google's OAuth servers. 
In the Google Cloud console, go to Menu menu > Google Auth platform > Clients. https://console.cloud.google.com/auth/clients

Click Create Client.
Click Application type > Web application.
In the Name field, type a name for the credential. This name is only shown in the Google Cloud console.
Add authorized URIs related to your app:
Client-side apps (JavaScript)–Under Authorized JavaScript origins, click Add URI. Then, enter a URI to use for browser requests. This identifies the domains from which your application can send API requests to the OAuth 2.0 server.
Server-side apps (Java, Python, and more)–Under Authorized redirect URIs, click Add URI. Then, enter an endpoint URI to which the OAuth 2.0 server can send responses.
Click Create.
The newly created credential appears under OAuth 2.0 Client IDs.

Note the Client ID.
**_Add it to the .env file where it says 'YOUR_CLIENT_ID'_**

**Create an API key**

In the Google Cloud console, go to Menu menu > APIs & Services > Credentials.
https://console.cloud.google.com/apis/credentials
Click Create credentials > API key.
Your new API key is displayed.
Click Copy content_copy to copy your API key for use in your app's code. The API key can also be found in the "API Keys" section of your project's credentials.
**_Add it to the .env file where it says 'YOUR_API_KEY'_**



**Run the sample**

In your working directory, install the http-server package:

    npm install http-server
In your working directory, start a web server:

    npx http-server -p 8000
In your browser, navigate to http://localhost:8000.

You see a prompt to authorize access:
If you're not already signed in to your Google Account, sign in when prompted. If you're signed in to multiple accounts, select one account to use for authorization.
Click Accept.

Your JavaScript application runs and calls the Gmail API.



future edits:
be able to undo deletes?

unsubscribe from this email button too? so it kills two birds with one stone

analyze top senders list so you know who to delete from (maybe with amount of mb they take up)
