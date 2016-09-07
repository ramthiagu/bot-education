## Cognitive Services Lab

## Pre-Requisites

1.  A Microsoft Account.  If you do not have one, please sign up for one [here](https://account.microsoft.com/about).

## Step 1:  Sign up for Cognitive Services trials

We are going to sign up for two Cognitive Services trial accounts:

* Entity Linking Intelligent Service (ELIS)
* Language Understanding and Intelligent Service (LUIS)
* Emotion API
* Face API
* Text Analytics API

To sign up, follow these instructions:

1.  Go to https://www.microsoft.com/cognitive-services/en-us/apis
*  Click on "My account" in the upper right-hand corner to log in to Cognitive Services. ![my cognitive services account](images/home_account_circle.PNG)
*  You will see a 'Hello' welcome page with a listing of trials from which you can request new ones.  Please select "Entity Linking", "Computer Vision", "Emotion", "Face", and "Text Analytics".  Read and agree to Microsoft Cognitive Services Terms and Microsoft Privacy Statement.  Click "Subscribe" to sign up for these trials.

## Step 2:  Open up the API Reference and testing console

1.  Using the upper navigation, click on the "Developers" drop-down menu item and select "Documentation".
2.  "Documentation" should have all of the APIs listed to the left.  Select `Computer Vision API`.  A selection list will expand.
3.  From the expanded list, select `API Reference`.
4.  Here you should see a button "Open API Testing Console".  Click this (shown in red, here).  ![open testing console](images/api_ref_testing_console_open.PNG).

## Step 3:  Analyze an image in the testing console

Here we will formulate our request, send it and interpret the response.

1.  Ensure that on the left, `Analyze Image` POST is selected.
*  Under "Query parameters", change `visualFeatures` to "Tags" to get all of the "tagging" or people/places/things information.
*  Under "Headers", keep the `Content-Type` as "application/json" because we are sending our request content as a serialized JSON query.  Fill in the `Ocp-Apim-Subscription-Key` with the key given by the trial (you may have to go back to your "My account" page as you did in the signing up instructions above).
*  Under "Request body", read through the information and image requirements.  In the text box replace the URL value string with this image string:  "https://raw.githubusercontent.com/michhar/bot-education/master/misc/tmp/images/man_with_frisbee_beach.jpg".
*  Scroll down past the HTTP request (noticing how the request was built for us here) and click on "Send".
*  Look for a 200 Response status and if you did not recieve this "OK" response status, check the error message and fix what is needed.
*  Once successful, take a look at the "Response content" for "Description" analysis.  Notice the "captions" and how this returns a natural language representation of what is present in the image.


**Take a screenshot of the response JSON and send this information to the appropriate party for homework collection, making sure to include the timestamp.**

In addition to this lab, try the console with different images as well as exploring "OCR" or "Describe Image" for instance.  Note that many of the Cognitive Services APIs have this testing console interface and it is valuable for understanding the kind of information needed in a request and expected in response.


