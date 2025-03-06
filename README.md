# Before you start
You can download a ZIP file along with two CSV files ("Request" and "Absence Type"). Before using the app, you need to create a SharePoint list.

You can choose your e-mail in the EmailAdmin environmental variable, so the flow will automatically send you e-mails as new requests is sent.

How to Set Up the SharePoint List:
- Select your desired SharePoint site.
- Click "Add new list" → "From existing CSV file".
- Choose the provided CSV file.
- This will automatically create all the necessary columns for you. It happens sometimes that automatic csv creation fails and some issues might occur.
- Now, you need to make sure to set up both lists with appropriate changes:
  "Absence Type" list should looks like this:
![AbsenceType1](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint_Hint1A.jpg)

-But after import might look like this:

![AbsenceType2](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint_Hint1.jpg)

  "Request" list should looks like this (most common issue is lack of ID (numeric) column. Sometimes it might be necessary to add it:
![AbsenceType2](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint%20Hint2.jpg)


Connecting the App to SharePoint:
- The app uses Environmental Variables for SharePoint connections.
- When launching the app, you will be prompted to select your own SharePoint list.
- Enjoy using the Absence Manager app! 🚀


# Absence Manager
The Absence Manager is a fully responsive (tablet and mobile version) Power Platform application built with Power Apps, customized with Power Automate flow and connected to a SharePoint lists to manage absence requests. The original app was created during the Udemy course, however substantial approvment were added, including: Power Automate flows and responsive design.

This README provides an overview of the app’s features and functionality.
## Features
The Absence Manager app consists of multiple screens that provide a comprehensive absence management solution.

With this app, users can:
✅ Add new request for days off
✅ View pending requests and track number of remain days off
✅ Manager has a previlage to decide about the requested days off - it is possible to make it directly from the app or by e-mail automatically send when new request is submitted.

#### ⏳ Loading Screen:
- Loads all essential app styles as global variables (OnVisible property).
- A timer ensures that all global variables are properly loaded before navigating to the Home Screen.
![Loading Screen](https://github.com/BMirska/AbsenceManager/blob/main/Zrzut%20ekranu%202025-03-06%20132310.png)
#### 🏠  Screen 1 'Home Screen':
- Left navigation panel → Allows users to select screen for new Request ("Request Absence"). Manager can go directly to management of pending requests "Approve requests".
- Main content → User can track the numbers of left number of days off, the number of sent requests and number of requests currently in approval. Below he can easily scroll through Pending requests. Manager see also second gallery "Request to Approve"
- Tablet versions:
  
![Home Screen Tablet Horizontal](https://github.com/BMirska/AbsenceManager/blob/main/Home%20Screen%20Horizontal%20Tablet.jpg)
![Home Screen Tablet Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Vertical%20Tablet.jpg)

- Mobile version:
  
![Home Screen Tablet Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Absence%20Screen%20Mobile.jpg)


#### 👤 Screen Request Absence
- Users request a new absence in Request Absence Screen. They can choose the absence type, dates (from - to) and deputy (if needed). They can provide additional comments to the approver. Approver is set automatically (persons manager). 
- Upon clicking "Submit" button the request is send to SharePoint list with "In progress" status and waiting for the approval.
- Power Automate flow is sending approval e-mail to the manager and now he can can decide through e-mail. He wants to approve or reject the request..? Now it's time for the decision!
- When manager decide whether he allows the person take some days off the requester is getting his answer right away with a short e-mail. He is informed whether his approval was approved or rejected :)
- The status in the sharepoint list is automatically changes from "In progress" to "Approved" or "Rejected"

Of course, the screen is fully responsive, so it can be managed online, on tablet or mobile phone:


![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Absence%20Horizontal%20Tablet.jpg)

![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Abcence%20Vertical%20Tablet.jpg)
![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Absence%20Screen%20Mobile.jpg)

#### 📋 Screen Pending Request
- Here manager can see how many request is pending and decide which one he wants to manage..

![Pending Request Horizontal](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Horizontal%20Tablet.jpg)
![Pending Request Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Vertical%20Tablet.jpg)
![Pending Request Mobile](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Mobile.jpg)

#### ✅ Screen Decide
- When manager click on "Pending Request Screen" Decide Button, he is launched to "Decision Screen". Here he can directly decide about requests.
  

### 🚀 Summary
The Absence Manager App streamlines absence management with:
✅ Easy request submition
✅ Pending request management 
✅ Is fully responsive
✅ Has Power Automate customization 


