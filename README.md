# Before you start
You can download a ZIP file along with two CSV files ("Request" and "Absence Type"). Before using the app, you need to create a SharePoint list.

You can choose your e-mail in the EmailAdmin environmental variable, so the flow will automatically send you e-mails as new requests is sent.

How to Set Up the SharePoint List:
- Select your desired SharePoint site.
- Click "Add new list" → "From existing CSV file".
- Choose the provided CSV file.
- This will automatically create all the necessary columns for you. 
- If the automatic import fails, some columns might be missing. You will need to manually adjust:
  "Absence Type" list should looks like this:
![AbsenceType1](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint_Hint1A.jpg)

-But after import might look like this:

![AbsenceType2](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint_Hint1.jpg)

The "Request" list should have a numeric ID column. If missing, you must add it:
![AbsenceType2](https://github.com/BMirska/AbsenceManager/blob/main/SharePoint%20Hint2.jpg)


Connecting the App to SharePoint:
- The app uses environmental variables for SharePoint connections.
- Upon launching the app, you will be prompted to select your SharePoint list.
- Enjoy using the Absence Manager app! 🚀


# Absence Manager
The Absence Manager is a fully responsive (tablet and mobile version) Power Platform application built with Power Apps, customized with Power Automate flow and connected to a SharePoint lists to manage absence requests. The original app was created during the Udemy course, however substantial approvements were added, including: Power Automate flows and responsive design.

This README provides an overview of the app’s features and functionality.
## Features
The Absence Manager app consists of multiple screens that provide a comprehensive absence management solution.

The Absence Manager app offers a comprehensive absence management solution with the following key features:
✅ Add new request for days off
✅ View pending requests and track number of remain days off
✅ Manager has a previlage to decide about the requested days off - it is possible to make it directly from the app or by e-mail automatically send when new request is submitted.

#### ⏳ Loading Screen:
- Loads all essential app styles as global variables (OnVisible property).
- A timer ensures that all global variables are properly loaded before navigating to the Home Screen.
![Loading Screen](https://github.com/BMirska/AbsenceManager/blob/main/Zrzut%20ekranu%202025-03-06%20132310.png)
#### 🏠  Screen 1 'Home Screen':
- Left navigation panel for selecting screens (e.g., "Request Absence" or "Approve Requests").
- Displays remaining days off, sent requests, and pending approvals.
- Tablet versions:
  
![Home Screen Tablet Horizontal](https://github.com/BMirska/AbsenceManager/blob/main/Home%20Screen%20Horizontal%20Tablet.jpg)
![Home Screen Tablet Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Home%20Screen%20Vertical%20Tablet.jpg) 

- Mobile version:
  
![Home Screen Tablet Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Home%20Screen%20Vertical%20Mobile.png)


#### 👤 Screen Request Absence
- Users can request a new absence, specifying dates, type, and deputy..
- Upon clicking "Submit" button the request is send to SharePoint list with "In progress" status and waiting for the approval.
- Power Automate sends approval emails to the manager.
- When manager decide whether he allows the person take some days off the requester is informed via e-mail whether his approval was approved or rejected,
- Status updates automatically in SharePoint upon approval or rejection.

Of course, the screen is fully responsive, so it can be managed online, on tablet or mobile phone:

![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Absence%20Horizontal%20Tablet.jpg)

![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Abcence%20Vertical%20Tablet.jpg)
![Screen Request Absence ](https://github.com/BMirska/AbsenceManager/blob/main/Request%20Absence%20Screen%20Mobile.jpg)

#### 📋 Screen Pending Request
- Managers can view and manage pending requests.

![Pending Request Horizontal](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Horizontal%20Tablet.jpg)
![Pending Request Vertical](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Vertical%20Tablet.jpg)
![Pending Request Mobile](https://github.com/BMirska/AbsenceManager/blob/main/Pending%20Request%20Screen%20Mobile.jpg)

#### ✅ Screen Decide
- When manager click on "Pending Request Screen" Decide Button, he is launched to "Decision Screen". Managers can approve or reject requests directly.
  

### 🚀 Summary
The Absence Manager App streamlines absence management with:
✅Simplifies absence requests.
✅Allows easy management of pending requests.
✅Is fully responsive across tablet and mobile.
✅Integrates Power Automate for seamless approval workflows.


