## Project Overview
The Salesforce Tours & Travels Customer Relationship Management (CRM) Platform is a customized solution developed to support the core operations of a travel and tours business using Salesforce’s powerful CRM tools. This system is designed to help manage client inquiries, tour package selections, bookings, payments, and post-travel feedback all within a centralized platform. By automating routine tasks such as booking approvals, customer updates, and task reminders through tools like Flows and Process Builders, the platform improves efficiency and accuracy. It also improves the customer experience by delivering tailored communication and ensuring safe management of data, while supporting the business with real-time insights through interactive reports and dashboards. This project aims to deliver a reliable, scalable system that empowers travel agencies to serve clients more effectively and grow their operations with ease.

![Tours](https://github.com/user-attachments/assets/c6df51b7-5009-4642-8cbe-78ce35dbb12f)



## Documentation Links and References

# Tours and Travel Salesforce Documentation: [Click Here](https://docs.google.com/document/d/1XI8Alpxqr7h0QWFfXDy-89Z98Hb3c_0oS7_Yk6difD4/edit?usp=sharing)
# Video Presentation: [Click Here](https://drive.google.com/drive/folders/1USzop2dOfdSFhZ4mGcKomYQPCLnyBA02?usp=sharing)

## Phase 1: Requirement Analysis & Planning

During the Requirement Analysis & Planning phase of my Tours and Travels CRM project, I focused on gaining a deep understanding of the travel domain, its business processes, and user expectations. I gathered and analyzed system requirements to define what the platform needed to deliver for both travel agents and customers. From this analysis, I was able to outline a clear project scope and build a technical roadmap that served as the foundation for the entire development process. This early planning ensured that the CRM would be scalable, well-structured, and aligned with real-world travel operations, setting the stage for efficient implementation and future growth.

### Understanding Business Requirements

I began by analyzing how global tours and travel agencies operate, focusing on challenges like manual bookings, poor communication, and limited tracking. By gathering input from stakeholders and studying relevant resources, I identified key requirements such as automating workflows, managing bookings by region, and improving customer engagement through feedback and reporting.

### Defining Project Scope & Objectives

The goal was to build a scalable, role-based CRM that supports the entire booking lifecycle—from inquiry to feedback. My objectives were to reduce manual work, streamline operations, enhance customer experience through automation, and provide actionable insights via reports and dashboards.

### Gathering & Analyzing User Needs

I collected user needs from key roles like customers, agents, guides, finance, and admins. Tools like Google Forms, user personas, and journey mapping helped me understand expectations like simple onboarding, personalized booking options, and dynamic pricing based on membership tiers.

### Identifying Key Salesforce Features & Tools Required

To meet business needs, I selected relevant Salesforce tools including custom objects, Flows, Apex classes, LWC components, and analytics features. I also designed automation processes and integrated approval workflows, ensuring flexibility, scalability, and a responsive UI.

### Designing Data Model and Security Model

I designed a relational data model linking customers, bookings, packages, payments, guests, and feedback. Security-wise, I implemented role hierarchies, custom profiles, field-level permissions, and sharing rules to ensure appropriate data access across different user types.

## Phase 2: Salesforce Development – Backend & Configurations

In this phase, I developed the core functionality of the Tours and Travels CRM by configuring standard Salesforce features and building custom backend logic. I used Flows and Process Builders to automate tasks like booking confirmations, feedback collection, and payment status updates. Where complex logic was needed—like bulk operations or real-time record creation—I implemented Apex triggers, batch jobs, and future methods. I also configured roles, profiles, permission sets, and sharing rules to secure data access based on user type. This backend setup ensured that the CRM operates smoothly, handles data efficiently, and supports scalable business processes.

### Milestone 1: Salesforce Account
For the initial milestone of Phase 2, I began by creating a Salesforce Developer Edition account to serve as the foundation for building the Tours and Travels CRM. I signed up through the official Salesforce developer site by providing my personal and academic details, including my name, email, and college name as the organization. After submitting the form, I received a verification email, which I used to activate my account. Once verified, I set my password and configured security settings to complete the setup process. This granted me access to the Salesforce Setup environment, where I would configure objects, implement automations, and write custom logic. Establishing this developer org was essential for simulating a real-world CRM project in a controlled, development-focused environment. It also allowed me to explore and apply Salesforce’s features hands-on, preparing for the configuration and development work ahead.
<img width="1540" height="930" alt="Account Activation" src="https://github.com/user-attachments/assets/d7002bdc-2509-4438-b3bd-7a1af80326d8" />

### Milestone 2: Objects Creation
I created the core custom objects needed to support the functionality of the Tours and Travels CRM system. Starting with Customer Info, I defined the object label, record name, and enabled reporting, search, and field history tracking to ensure usability and data traceability. I proceeded to build other critical objects: Booking, BookingGuest, TravelPackage, Booking Payment, Employee, and Feedback, each tailored to capture specific data relevant to travel operations. These objects were designed with the necessary field types and relationships to support automation, reporting, and user interactions. The setup ensures that customer records, travel details, and transactions are logically structured and easy to manage across various roles within the CRM.
<img width="1920" height="1000" alt="All bookings" src="https://github.com/user-attachments/assets/28ff5894-d634-4e5b-8a62-234b1961a32a" />
<img width="1916" height="989" alt="Customer Info" src="https://github.com/user-attachments/assets/b5fab3f4-8563-490b-97e2-78ec4ddd2b70" />
<img width="1920" height="994" alt="Travel Package" src="https://github.com/user-attachments/assets/b9cd1fa4-cb51-4063-8e59-bc68c169ff5c" />

### Milestone 3: Tabs
To make the custom objects accessible in the UI, I created custom tabs for each one. I started with Customer Info, navigating to the Setup page and selecting "Tabs" from the Quick Find bar. Under the Custom Object Tabs section, I created a new tab by selecting the Customer Info object, choosing a tab style, and proceeding through the wizard. On the profiles and custom app steps, I kept the default settings, ensured the "Append tab to the user's existing personal customizations" option was selected, and saved the configuration.

After completing the Customer Info tab, I followed the same procedure to create tabs for the remaining objects: Booking, Booking Guest, Travel Package, Payment, Employee, and Feedback. Each tab was configured to provide easy navigation and visibility for users, while allowing administrators to manage access through profiles and app assignments. This step was crucial in ensuring all custom objects are visible and accessible for users within the Tours and Travels CRM.
<img width="1920" height="985" alt="Tabs" src="https://github.com/user-attachments/assets/76ce7e9e-3cfc-4ace-a6c4-5f13a3f54abd" />

### Milestone 4: Fields & Relationships
In this milestone, I designed and implemented all necessary fields and relationships across the custom objects used in the Tours and Travels CRM. For the Customer Info object, I created an Email field with the proper data type and ensured reporting and search capabilities were enabled. To support global data, I configured a Global Picklist Value Set for countries and reused it across related fields for consistency.

I established relationships between objects to maintain data integrity, such as a Lookup Relationship from the Booking object to Customer Info. Additionally, a Formula Field was added in the Booking Guest object to categorize age groups dynamically. Important picklists like “Relation with Customer” and “Availability Status” were created to capture relevant business data points.

To reflect real-world travel industry features, I configured multi-select picklists for fields like Membership, Package Type, and Transportation Modes. These fields allow flexible package definitions. For employee roles and departments, I defined comprehensive picklists covering common travel and support functions. Language capabilities, assigned regions, and location fields (country and city) were also configured using global picklist value sets for consistency and scalability.

Finally, I created fields related to payments and feedback, including a “Payment Method” picklist with standard options. All field types were carefully selected to match data requirements and business rules, supporting efficient operations and data collection within the CRM.
<img width="1920" height="1080" alt="Milestone 4 (Customer Info)" src="https://github.com/user-attachments/assets/ab5cdf61-5ffc-4936-8093-94b94ff9e234" />
<img width="1920" height="1080" alt="Milestone 4 (Booking Guest)" src="https://github.com/user-attachments/assets/9359cac4-ddeb-4ed6-838f-01ce3605bed5" />
<img width="1920" height="1080" alt="Milestone 4 (Travel Package)" src="https://github.com/user-attachments/assets/90106412-1234-47fa-b21d-d8ea0a7bf490" />

### Milestone 5 : Field Dependencies
I configured field dependencies to streamline data entry and improve accuracy across key objects in the Tours and Travels CRM. Within the Booking Guest object, I linked the Country field as a controlling field to the City field, ensuring that only relevant cities are displayed based on the selected country. This enhances user experience by dynamically filtering location options during data entry.

For the Booking object, I created a dependency between Membership and Preferred Accommodation. This setup ensures that accommodation options like hotels, villas, or resorts are filtered based on the customer's membership level (Basic, Gold, or VIP), reinforcing business logic during booking creation.

In the Employee object, I established a dependency between Department and Role. This allows roles such as Travel Agent, Finance Executive, or Tour Coordinator to appear only under their appropriate departments like Travel Operations, Finance, or Logistics. These dependencies collectively help maintain clean data input and enforce logical consistency across the system.
<img width="1920" height="992" alt="Field Dependency Booking Guest" src="https://github.com/user-attachments/assets/f0b35780-f8ce-4543-9900-8bee62566a86" />


### Milestone 6 - Validation Rules
Several Validation Rules were configured to maintain data accuracy and enforce key business logic throughout the Tours and Travels CRM. For the Customer Info object, constraints ensure phone numbers are exactly 10 digits, emails follow proper formatting, and dates of birth are not set in the future. The Booking Guest object restricts age inputs to values above zero and conditionally requires emails based on assigned roles.

In the Employee object, guides must have at least one selected language, reinforcing role-specific completeness. Additionally, the Booking object enforces that every new booking record defaults to a "Pending" status. These validations help prevent data entry errors and ensure consistency across records before submission.
<img width="1920" height="992" alt="Validation Customer Info" src="https://github.com/user-attachments/assets/015f5178-e5d1-46d8-8f84-c22e52d38613" />

### Milestone 7: Approval Process
I began by preparing all prerequisites—creating profiles, roles, and users—before setting up the approval process. I created a classic email template to notify managers when a booking cancellation request is submitted. The email includes key booking details and prompts the approver to log in and take action.

Next, I made two additional templates: one for approved cancellations and another for rejections. These are sent to customers with personalized booking details and status updates, ensuring clear communication throughout the process.

Then, I created the actual approval process on the Booking object using the standard wizard. I defined entry criteria to trigger the process only when the booking status is “Cancelled” and the cancel confirmation checkbox is true.

I assigned the approval to a specific user and selected the first email template for assignment notifications. I configured the approval page to display essential fields like booking number, travel package, and cancellation reason.

Travel agents and booking owners were set as the initial submitters. Upon submission, the status updates to “Pending.” If approved, the system changes the approval status to “Approved” and sends an approval email. If rejected, the status returns to “Confirmed” and a rejection email is sent.

Finally, I added a single approval step for the Travel Agent Manager and activated the process. This setup ensures cancellation requests are properly reviewed and customers are promptly informed of the outcome.
<img width="1920" height="993" alt="Classic Email Template Booking Cancellation" src="https://github.com/user-attachments/assets/6c0359d3-ad1b-4aa0-979e-289603b4b25c" />
<img width="1920" height="988" alt="Approval Processes Booking" src="https://github.com/user-attachments/assets/268ac9b3-140f-4272-8467-92fe1ece8dae" />

### Milestone 8 - Flows
To ensure data accuracy, I created a record-triggered flow that prevents users from adding more guests than the number of travelers specified in a booking. I started by creating a new Record-Triggered Flow for the BookingGuest object, setting the trigger to fire on both record creation and update.

I used a Get Records element to retrieve the related Booking record and all its fields. After that, I added a Decision element to compare the number of existing BookingGuest entries with the total travelers defined in the booking. If the number of guests exceeded the number of travelers, the "Yes" outcome path was followed.

I then created a Text Template resource named ErrorMessageTemplate to display a clear error:
“Sorry, we can't add more guests because the maximum number of Travellers for this booking has already been reached.”

Under the "Yes" outcome, I added a Custom Error element and configured it to show the message in a pop-up window on the record page. After saving and activating the flow, the setup successfully prevents users from overbooking guests, helping maintain business rules and system integrity.
<img width="1919" height="990" alt="Flows Final Output (ERROR IF GUEST GREATER THAN TRAVELLERS)" src="https://github.com/user-attachments/assets/4b809e3c-1fda-497a-b8e7-3ca104655b55" />

### Milestone 9 - Workflows
To automate follow-ups, I created a workflow rule that triggers a task for the travel agent whenever a booking is marked as Completed. I navigated to Setup, searched for Workflow Rules, and created a new rule for the Booking object.

I named the rule Follow-up Task After Booking Completion, set it to trigger when records are created or edited, and defined the criteria as: Booking Status equals Completed.

Next, I added a New Task action. I assigned the task to the Booking Owner, set the subject to Follow up for feedback, and configured the Due Date to be 3 days after the Travelling End Date. The task priority was set to Normal, status to Not Started, and included a note requesting the agent to contact the customer for feedback.

Finally, I saved the task and activated the workflow.
<img width="1915" height="993" alt="Workflow rules Follow-up Task After Booking Completion" src="https://github.com/user-attachments/assets/6823b406-aea5-46d1-95a5-fd8691f10b2b" />

### Milestone 10 - Process Builder
To streamline operations in the Tours and Travels CRM, I built a Process Builder automation that updates the Booking Status to Confirmed once a related Payment is marked as Completed. From Setup, I opened Process Builder, created a new process named Update Booking to Confirmed When Payment Completed, and set it to start when a record changes.

I selected Booking Payment as the triggering object and configured it to run on record creation or edit. For the criteria, I defined a condition: Payment_Status__c equals Completed, using the AND logic.

Next, I added an immediate action to Update Records. I chose the related Booking record, and set the Booking Status field to Confirmed. After saving everything, I activated the process to ensure the automation runs in real time.
<img width="1917" height="902" alt="My process builder final output" src="https://github.com/user-attachments/assets/619365b6-94f7-46b1-b275-ab2286e8d1d8" />

### Milestone 11 - Triggers
In this milestone, I created an Apex Trigger to automate two tasks whenever a new booking is inserted.

First, I logged into Salesforce with admin access, then opened the Developer Console from Setup. I created a trigger on the Booking__c object named BookingTrigger, which runs after insert. This trigger calls a handler class, BookingTriggerHandler, where I added a method to automatically create a Booking Payment record for each new booking with the default payment status set to 'Pending'.

Next, I enhanced the same trigger to include the creation of Booking Guest records. In the same handler class, I defined the createBookingGuests method, which reads the Number_of_Travelers__c field from each new booking and inserts that many guest records linked to the booking. Each guest is labeled as Guest 1, Guest 2, and so on.

After writing and saving both the updated trigger and the Apex class, the automation now ensures that every new booking creates both a Booking Payment and the appropriate number of Booking Guests automatically.
<img width="1915" height="995" alt="BookingTrigger Developer Console" src="https://github.com/user-attachments/assets/42d5ae3d-a9b9-42b6-b80b-e24a22746597" />

### Milestone 12 - Asynchronous Apex
I automated three critical email notifications using asynchronous Apex to ensure non-blocking operations and scalability.

First, I created a future method in an Apex Class (BookingConfirmationEmailer) that sends a confirmation email when a booking status changes to “Confirmed.” I updated the existing BookingTrigger to detect the status change and call this method, passing the affected booking IDs.

Second, I implemented a Queueable Apex class (BookingReminderQueueable) to send tour reminders three days before the tour start date. I then created a Schedulable class (BookingReminderScheduler) that queries bookings with a travel date exactly three days ahead and queues the reminder job. I scheduled this job to run daily at 6 AM using a CRON expression.

Lastly, I built a Batch class (PaymentReminderBatch) to send payment reminders for bookings marked as “Pending” if they were made yesterday. I added a finish method to notify the admin once the job runs. I wrapped this in another Schedulable class (SchedulePaymentReminderBatch) and configured it to run every day at 5 AM via the UI Apex scheduler.

With this setup, all key notifications—confirmation, tour reminders, and payment follow-ups—are handled automatically and efficiently.
<img width="1914" height="995" alt="Activity 1 Future asynchronous apex" src="https://github.com/user-attachments/assets/61b4fd7a-5b21-49cb-ab1b-99684f7ce76b" />

## Phase 3: UI/UX Development & Customization
In Phase 3, I focused on developing a clean, responsive, and intuitive user interface for the Tours and Travels CRM. I designed and built custom Lightning Web Components (LWC) and Lightning pages to enhance user experience across desktop and mobile. I also configured user authentication and used Salesforce Flows to streamline navigation and automate key UI actions.

To improve usability, I customized page layouts, dynamic forms, and applied conditional visibility where needed. I also tailored dashboards and reports to ensure users could access relevant insights quickly. Finally, I tested all UI elements for functionality and responsiveness, ensuring a seamless experience for end users.

### Milestone 13:The Lightning App
In Milestone 13, I created a custom Lightning App named "Tours & Travels CRM" to streamline navigation and centralize key modules. Using the App Manager, I uploaded a relevant image for branding and proceeded with default app and utility settings. I then added essential objects like Customers Info, TravelPackages, Booking, Booking Payments, BookingGuests, Employees, Feedback, Tasks, Reports, and Dashboards to the app.

Lastly, I assigned the System Administrator profile to ensure appropriate access, and completed the setup by saving and activating the app.
<img width="1920" height="993" alt="App details   Branding" src="https://github.com/user-attachments/assets/3be27382-677e-4bce-a285-33a459392f27" />

### Milestone 14 -Editing of Page Layouts
In this phase, I focused on enhancing the layout structure of various standard and custom objects within the Tours and Travels CRM to ensure a more intuitive and user-centered interface. Using the Object Manager in Salesforce Setup, I accessed the layout settings for key objects including Customer Info, BookingGuest, TravelPackage, Employee, Booking, Booking Payments, and Feedbacks.

For each object, I carefully arranged and grouped fields in a way that aligns with how users interact with the system. This included placing the most frequently used and essential fields in more prominent positions, while secondary or supporting fields were organized logically below. The adjustments aim to improve data readability, reduce input errors, and make navigation more seamless for users.

After making the necessary changes to each object’s layout, I saved the configurations to reflect the updates in the live environment. These layout improvements contribute to a cleaner interface and a more efficient workflow for all CRM users.
<img width="1916" height="973" alt="Customer Info page layout" src="https://github.com/user-attachments/assets/dc9a25cb-397b-4922-94dd-7dc01046cf0c" />

### Milestone 15 - Dynamic Forms
To enable dynamic field visibility based on booking status, access the Tours & Travels CRM App via the App Launcher and navigate to the Booking tab. Create and save a new booking record to work with. After saving, open the record, click the gear icon in the upper-right corner, and select Edit Page to launch the Lightning App Builder.

Within the builder, locate the Details section and click Upgrade Now on the right pane to enable Dynamic Forms for the Booking object. Select the Booking Page Layout when prompted, then proceed by clicking Finish. Once enabled, specific fields can be configured with visibility filters to display only under certain conditions.

Start with the Cancellation Date field. Apply a filter so that this field is visible only when the Booking Status equals Cancelled. Repeat the same process for the Cancel Confirmation and Approval Status fields, ensuring they also appear only when the booking status is set to Cancelled.

After setting the filters, save your changes and click Activate. Choose Org Default, enable the form for both Desktop and Phone views, and complete the setup by clicking Next followed by Save. This ensures a streamlined and dynamic user experience for managing booking details based on booking status.
<img width="1915" height="1032" alt="Dynamic Forms" src="https://github.com/user-attachments/assets/aaaf741e-9076-4636-a8e3-b5553d40f6c1" />

### Milestone 16 : Users
Before creating users, ensure that the Profiles and Roles milestones are completed, as these are prerequisites for assigning appropriate access levels. Once ready, navigate to Setup, type Users into the Quick Find box, and select Users. Click New User to begin entering user details.

Start by creating a user with the following information: enter Michael as the First Name and Jackson as the Last Name. Provide an alias, a valid personal email address, and a unique Username in the format text@text.text. Assign a nickname for easier identification within the system. Set the Role to Travel Agent Manager Role, the User License to Salesforce Platform, and the Profile to Travel Agent Profile.

After saving, repeat the process to create additional users. For the next set, assign the Role as Travel Agent Role, with the same User License (Salesforce Platform) and Profile (Travel Agent Profile). It is recommended to create at least two users for each defined role, ensuring that all necessary team members are represented with appropriate access in the system.
<img width="1919" height="995" alt="All users" src="https://github.com/user-attachments/assets/5ead124c-cc77-4fe5-a886-139551e46249" />

### Milestone 17 : Reports
To begin setting up reports, open the App Launcher, search for Reports, and click on the Reports tab. Create a new folder by clicking New Folder, entering Revenue Folder as the folder label. The unique name will auto-populate. Click Save to create the folder.

Next, locate the newly created Revenue Folder by navigating to the All Folders section within the Reports tab. Click the dropdown arrow beside the folder name, select Share, and choose to share the folder with roles. In the Name field, search for and select Travel Agent Manager Role and Finance Officer Role, assigning View access for both. Confirm by clicking Share, then Done.

Before building reports, ensure that you have added at least 10 new records per object, filling in all available fields for more accurate data. When creating records in the Booking object, ensure the Booking Status is set to Pending to meet filter requirements for specific reports.

For Report 1, go to the Reports tab and click New Report. Under the category “All,” search for and select Booking, then click Start Report. In the Columns section of the outline pane, include Booking Number, Customer, Booking Date, and Total Billing Amount, removing any unnecessary fields. Enable Update Preview Automatically and apply the following filters: Show Me = All Bookings, Booking Date = This Month, and Booking Status = Confirmed or Completed.

To categorize revenue, click the dropdown on Total Billing Amount, choose Bucket This Column, and define a Bucket Label called Revenue Category with ranges: Low (0–50,000), Medium (50,001–200,000), and High (>200,000). Apply this bucket and group the rows by Travel Package and Revenue Category. Add a Pie Chart, then click Save, naming the report Monthly Revenue Report. Save it in the Revenue Folder.

Continue by creating the following reports and organize each into relevant folders:

Report 2: Pending Payments – Tracks bookings with pending payments. Use the Booking Payments with Bookings report type and filter by Payment_Status__c = Pending. Add appropriate columns and save it in the Revenue Folder.

Report 3: Top Travel Packages (By Booking Count) – Identifies the most popular packages. Use the Bookings with Travel Packages report type, group rows by TravelPackage__r.Name, summarize by Booking count, and sort by the highest count. Save this report as Top Travel Packages.

Report 4: Employee Roles Distribution – Displays the number of employees per role. Use the Employees report type, group by Role__c, and add a Count Summary. Save this as Employee Role Breakdown.

Finally, create at least five additional reports tailored to different use cases or business needs to enhance your insights and reporting coverage across the Tours and Travels CRM system.
<img width="1920" height="1032" alt="Activity 3 Create Report " src="https://github.com/user-attachments/assets/7a6e76e4-b3cf-42fc-8115-39c899f49735" />
<img width="1920" height="542" alt="Activity 4 Create Other Reports" src="https://github.com/user-attachments/assets/885a0a2e-2ff6-43b2-a384-faa15dcd9b20" />

### Milestone 18 - Dashboards
To begin building dashboards for the Tours & Travels CRM, navigate to the Dashboards tab from within the application. Click New Dashboard, name it Tours & Travels Dashboard, and then click Create. Once the canvas loads, click on +Widget to add your first component. Choose the Monthly Revenue Report created in the earlier reports milestone. For visualization, select a Pie Chart, set the Max Values Displayed to 10, enter the subtitle as Total payments completed Bookings, and choose the Dark Theme for the widget. Click Add, then click Save to preserve your dashboard configuration.

Next, add three more components using any of the reports created under Activity 4 of the Reports Milestone. You may use different visualization types such as bar charts, line graphs, or tables based on your data and reporting needs. Each component should represent distinct insights to provide a comprehensive view of your system data.

To view your completed dashboard, open the App Launcher, search for Tours & Travels CRM, and click on it. From there, open the Dashboards tab and select Tours & Travels Dashboard to see a visual representation of the records. Although the sample screen may only show one component, ensure that your dashboard includes four fully configured components for a complete setup.

Lastly, create two additional dashboards using the other reports developed from Activity 4 of the Reports Milestone. These should highlight key metrics or insights that are most relevant to different roles or business areas within the CRM platform.
<img width="1920" height="1033" alt="Activity 1 Create Dashboard" src="https://github.com/user-attachments/assets/62366974-b4b4-4b4b-8b42-2139709d9495" />

### Milestone 19: Lightning Web Component Creation
This milestone introduces a dynamic UI enhancement in the Tours and Travels CRM using Lightning Web Components (LWC). The objective is to display travel packages based on the country selected by the customer on the booking form, updating the interface in real-time without refreshing the page. To begin, an Apex controller named TravelPackageController is created using the Developer Console. This controller defines a getPackagesByCountry method that returns a list of travel packages filtered by the selected country, using a @AuraEnabled annotation for client-server interaction.

Once the backend logic is ready, the next step involves creating a Lightning Web Component named TravelPackageSelector. Using tools like Lightning Studio (installed via Chrome extensions), the component structure is set up, including HTML, JavaScript, CSS, and the metadata configuration file. The HTML file defines the user interface, featuring a lightning-combobox for country selection and dynamically rendered details of the filtered travel packages. In the JavaScript file, a method handleCountryChange() is implemented to call the Apex method when a user selects a country. The data returned is then rendered on the UI.

The component is configured to be available on the App Page, Home Page, and Record Page by updating the XML metadata file. Once deployed successfully, this LWC enables customers to instantly view available travel packages based on their selected destination, enhancing user interactivity and responsiveness in the CRM system. This integration of Apex and LWC ensures seamless real-time filtering with an intuitive frontend experience.
<img width="1920" height="1080" alt="Lightning studio extension" src="https://github.com/user-attachments/assets/c8674316-01f1-4c2c-b5fe-34fb9c1c7432" />
<img width="1919" height="1039" alt="Creating Apex Class " src="https://github.com/user-attachments/assets/9aa8d141-938b-44b0-b7b2-d27fa1514f43" />

### Milestone 20 : Lightning App Page Creation
I enhanced the user interface by embedding the custom Lightning Web Component into a dedicated Lightning App Page. After opening the Lightning App Builder from Setup, I created a new App Page and named it Travel Package Selector. I selected a single-region layout to keep the design clean and focused. Then, I dragged the travelpackageselector component into the layout and saved the page. To make it accessible, I activated the page and added it to the Tours & Travels CRM app. Finally, from the App Launcher, I verified that both the CRM app and the standalone app page were available. When accessed, this page allows users to select a country and view corresponding travel packages dynamically, improving user engagement and data visibility.
<img width="1920" height="1077" alt="Activation of travel package selector" src="https://github.com/user-attachments/assets/ffb625c3-80a8-4ce0-8302-e8f23cc7609e" />

## Phase 4: Data Migration, Testing & Security
In this phase, I focused on migrating data from existing systems into Salesforce while ensuring accuracy, integrity, and consistency. I implemented robust data validation rules and performed multiple rounds of testing—including unit testing, integration testing, and user acceptance testing (UAT)—to confirm the correctness of migrated records and the reliability of system functionality. Alongside testing, I configured key security measures such as role-based access, sharing rules, and field-level security to safeguard sensitive data and ensure compliance with organizational policies.

### Milestone 21: Field History Tracking
To ensure important data changes are properly monitored in the system, I enabled Field History Tracking for selected objects in the Tours & Travels CRM. On the Booking object, tracking was configured for the Number of Travelers, Booking Status, and TravelPackage fields, so any updates to these values are now captured in the history related list. For the TravelPackage object, tracking was applied to the Price Per Person and Availability Status fields to help maintain visibility into pricing and availability changes. This setup provides a reliable audit trail for critical booking and package information.
<img width="1920" height="1080" alt="Field History Tracking on Booking Object" src="https://github.com/user-attachments/assets/bd0a7514-e2d1-4a34-a8df-ea1796fffe20" />

### Milestone 22 - Duplicate and Matching rules
To prevent duplicate entries in the Customer Info object, a matching rule was created that checks for an exact match between a customer’s email and phone number. This rule, titled “Unique Email and Phone Number Combination,” ensures Salesforce identifies potential duplicates based on those two key fields. Enabling the “Match Blank Fields” option allows the system to evaluate records even when one of the fields is empty, improving accuracy during data entry. Once defined, the rule was saved and activated to begin monitoring the data.

After the matching rule was in place, a duplicate rule was added to determine how Salesforce should respond when duplicates are detected. Named “Unique Email and Phone,” this rule allows records to be created or edited even if duplicates are found but provides a warning message to users: “Email and Phone must be Unique.” This ensures that users are informed of duplicates without blocking their workflow. The previously created matching rule was linked within this duplicate rule for consistency, and the setup was finalized by saving and activating the rule. Together, these configurations help maintain clean, reliable customer data in the CRM.
<img width="1919" height="1080" alt="Creating Duplicate rule customer info object" src="https://github.com/user-attachments/assets/9dea4071-5e01-462a-8436-7e0900bad620" />

### Milestone 23 : Profiles
To manage access based on user roles in the Tours and Travels CRM, multiple custom profiles were created by cloning the base “Standard Platform User” and “Salesforce Platform User” profiles. For instance, the Travel Agent Profile was created by cloning “Standard Platform User.” After naming and saving the profile, edits were made to set the default app as Tours and Travels CRM, and object-level permissions were granted accordingly. The agent was given full Create, Read, and Edit rights on key objects such as Bookings, Booking Guests, Booking Payments, Customer Info, and Travel Package, while only read access was allowed for Employee and Feedback objects. Additionally, the session timeout was set to 2 hours of inactivity, and password policies were configured with no expiry and a minimum password length of 8 characters.

Next, a profile named Tour Guide was created from the “Salesforce Platform User” template. This role required limited access, so only Read permissions were provided for Bookings, Booking Guests, and Travel Packages. The default app was also set to the CRM to ensure the user lands in the correct workspace upon login.

Similarly, the Finance Officer Profile was configured to allow access needed for managing financial transactions. Cloned from “Salesforce Platform User,” this profile was given full access (Read, Create, Edit) to Bookings and Booking Payments, while Travel Packages and Employee objects were made view-only. This ensures finance users can process transactions but cannot alter package or HR data.

For the Marketing Executive Profile, a custom profile was set up to support promotional campaigns and travel package management. Full access was given to the Travel Package object, enabling the executive to create and modify offerings. Meanwhile, view-only access was granted to supporting objects like Bookings, Booking Guests, Customer Info, Employees, and Feedbacks, ensuring visibility without the risk of unintended changes.

Lastly, a Customer Service Rep Profile was created with a focus on managing feedback. The user was given full rights over the Feedback object while maintaining read-only access to Bookings, Customer Info, and Travel Packages. This configuration ensures customer service reps can respond to issues without overreaching into booking or sales data.
<img width="1919" height="1080" alt="Travel Agent Profile " src="https://github.com/user-attachments/assets/0a7290c8-e771-44b2-aac1-929b074c990d" />

### Milestone 24 : Roles & Role Hierarchy
To establish data access control and visibility in the Tours and Travels CRM system, a structured role hierarchy was configured beginning at the top with the Travel Agent Manager role. This was created by navigating to Setup > Roles, expanding the role tree under the CEO, and selecting “Add Role.” The label Travel Agent Manager was entered, and the role name was auto-generated. Once saved, this new role became the supervisory role for team members who manage travel bookings.

To build the team structure under the Travel Agent Manager, two additional roles were created. The first, labeled Travel Agent, was added directly under the Travel Agent Manager using the same “Add Role” function. This role represents the front-line staff responsible for handling booking requests. Similarly, a second subordinate role, Travel Tour Guide, was added under the same manager. This role is designated for personnel who lead and guide the travel groups but don’t require broad data visibility.

Further expanding the hierarchy, three more roles were created directly beneath the CEO to reflect other key departments. The Finance Officer Role was added first, tasked with overseeing financial transactions and payment records. Following that, the Marketing Executive Role was introduced to handle promotions, travel package listings, and analytics. Lastly, the Customer Service Rep Role was created for the support team, ensuring they can manage customer inquiries and feedback efficiently.

This organized role hierarchy ensures data access flows logically from top to bottom, allowing managers to oversee their subordinates' data while maintaining security and control across the organization. Let me know if you'd like a diagram to visualize this structure.
<img width="1920" height="1080" alt="Travel Agent Manager Role" src="https://github.com/user-attachments/assets/9302c414-565d-488a-9117-f440637006c1" />

### Milestone 25 : Permission Set
In this milestone, a custom Permission Set was created to grant additional access to users without altering their core profile settings. By navigating to Setup > Permission Sets, a new permission set was created and labeled “Extra Permission For Travel Agent Manager.” This permission set is intended to provide more flexibility and granular control over what specific users can access beyond their profile-based permissions.

Once the permission set was created, the configuration continued by selecting it and navigating to Object Settings. From there, the TravelPackage object was located and edited. The permissions for this object were adjusted to allow full access — Read, Edit, Create, and Delete (R/E/C/D) — ensuring that users with this permission set can fully manage travel packages.

After saving these changes, the permission set was then assigned to the appropriate user. This was done by selecting Manage Assignments, clicking Add Assignment, and choosing the user assigned to the Travel Agent Manager Role. This ensures that the manager has enhanced access without needing to modify the base profile. Using permission sets in this way allows for greater flexibility in user access control while maintaining security and best practices in role management.
<img width="1920" height="1078" alt="TravelPackage Permission set" src="https://github.com/user-attachments/assets/e9cbd608-24f0-4533-b7c2-19385ed19b10" />

### Milestone 26: Sharing Setting
To enhance data security and control access to customer records, a sharing rule was implemented on the Customer Info object. First, the organization-wide default (OWD) setting for Customer Info was modified to “Private.” This setting ensures that only record owners and users higher in the role hierarchy can access the records, unless specific sharing rules are created.

To allow necessary visibility across teams, a new sharing rule was added. This rule is designed to automatically share Customer Info records owned by users in the “Travel Agent Role” with users in the “Tour Guide Role.” The access level granted through this rule was set to “Read Only,” meaning tour guides can view customer details without modifying them. This approach balances security and collaboration by maintaining control over sensitive data while enabling visibility where needed.
<img width="1920" height="1079" alt="Customer Info Sharing Rule" src="https://github.com/user-attachments/assets/6754f761-0d78-470d-bfe2-cbae74e44473" />

### Milestone 27 - Test Classes
To ensure the correct functioning of the BookingTrigger and BookingTriggerHandler, a dedicated Apex test class named BookingTriggerTest was developed. This test class simulates a real-life scenario by first creating a sample customer and a travel package record. It then inserts a new booking linked to the created customer and travel package. The test verifies whether the trigger logic correctly creates associated Booking_Payment__c and BookingGuest__c records. Assertions are used to confirm that one payment record with a default status of "Pending" is created and that three guest records are generated, each corresponding to a traveler. The use of Test.startTest() and Test.stopTest() ensures proper isolation of trigger execution for performance and coverage measurement. This test not only validates trigger functionality but also contributes to deployment readiness by meeting Salesforce’s code coverage requirements.
<img width="1920" height="1080" alt="BookingTriggerTest Status CHECKED" src="https://github.com/user-attachments/assets/abf7514a-c2b9-4709-87ea-8ba7d3a5f468" />

### Milestone 28 : Preparing Test Cases & Fixing Defects
As part of the quality assurance process, several test cases were designed and executed to validate the core functionalities of the Tours and Travels CRM system. The first test focused on verifying the successful creation of a new customer. The tester navigated to the Customer object page, filled in all required fields, and saved the record. The expected outcome was that the new customer would be stored properly and listed in the Customers page. Any failures would likely be due to missing mandatory fields or restrictive validation rules.

The second test case ensured that bookings could be created successfully. After accessing the Booking object and entering all necessary fields, the record was saved. Upon creation, the system was expected to automatically generate a related Booking Payment record with a default payment status of “Pending” and a set of Booking Guest records matching the value in the “Number of Travelers” field. If any of these actions failed, the issue was likely caused by incomplete data, validation errors, or issues in the Apex code responsible for the automation.

Another critical test case was created to validate system automation when a payment status is updated. Specifically, when the Payment Status field in a Booking Payment record is changed to “Completed,” the corresponding Booking record should update its status to “Confirmed.” Additionally, the system should send a confirmation email to the customer indicating the successful booking and payment. If these updates do not occur, potential defects could stem from process automation issues, misconfigured Process Builders, or overlooked Apex logic. These tests ensure the platform behaves as expected and help in identifying and resolving issues before final deployment.
<img width="1908" height="985" alt="Email Confirmation" src="https://github.com/user-attachments/assets/6911aef4-12e7-4d35-96b2-d8f67c714541" />

### Milestone 29 : Data Import Wizard
To efficiently populate the Salesforce environment with initial data, the Data Import Wizard was used to import sample CSV files for the Customer Info, TravelPackage, and Employee objects. Each CSV file contained a minimum of 20 records, with all mandatory and relevant fields completed to ensure successful import. The process began by logging into Salesforce as an administrator and launching the Data Import Wizard from the Quick Find box. After selecting the appropriate object, such as Customer Info, the “Add new records” option was chosen, and the corresponding CSV file was uploaded. Field mapping was then reviewed—auto-mapped fields were verified and corrected manually where needed to ensure data accuracy.

Once the mapping was complete, the import process was initiated and monitored through the Bulk Data Load Jobs section under Setup. The same procedure was followed for the TravelPackage and Employee objects. Upon completion, records were reviewed to verify successful import and field accuracy across all objects. This data seeding process ensured a reliable dataset was available for further testing, reporting, and user interaction within the Tours & Travels CRM application.
<img width="1920" height="1079" alt="Customer Info Data bulk" src="https://github.com/user-attachments/assets/38c8a401-8db4-4c59-a38a-cb49d6d66274" />

## Phase 5: Deployment, Documentation & Maintenance

### Deployment Strategy
The deployment strategy for this Tours and Travels Salesforce CRM project focuses on simulating a real-world deployment process within a Developer Edition org. While no actual deployment to production is performed, all configurations, customizations, and testing follow standard practices used in enterprise environments. In real scenarios, deployment involves moving components from sandbox to production using tools like Change Sets, GitHub, or CI/CD pipelines to ensure controlled and error-free releases. This approach prepares us to understand structured deployment processes despite the limitations of a standalone Developer Org.

### System Maintenance and Monitoring
The system will be maintained and monitored through regular data validation, performance reviews, and user feedback. Administrators will oversee user roles, security settings, and ensure that automation (flows, triggers, and scheduled jobs) runs smoothly. Monitoring tools like audit logs, field history tracking, and error notifications will help detect issues early, while periodic updates and enhancements will ensure the system stays aligned with business needs.

### Troubleshooting Approach
The troubleshooting approach involves identifying, analyzing, and resolving system issues through a structured process. When an error occurs, logs and error messages are reviewed to determine the root cause. Common steps include replicating the issue, checking automation logic (flows, triggers, validation rules), verifying user permissions, and correcting data inconsistencies. Issues are documented, and solutions are applied and retested to ensure the problem is fully resolved.

### Future Enhancements
Future enhancements for the Tours and Travels Salesforce CRM may include integrating a chatbot to handle customer inquiries in real-time, improving response times and overall user engagement. This would allow customers to get instant assistance with bookings, travel packages, and general questions. AI-powered features such as intelligent travel package recommendations based on user preferences and booking history can further personalize the customer experience.
Additional improvements may involve mobile app integration to enhance accessibility, especially for users on the go. The system can also incorporate automated feedback analysis to quickly gather insights from customer reviews, and predictive analytics to identify booking trends and seasonal demands. These enhancements aim to elevate service quality, user satisfaction, and operational efficiency.	

## Conclusion
The Tours and Travels CRM project showcases how Salesforce can be effectively utilized to digitize and enhance travel and tour operations. By implementing custom objects, automation processes, Lightning components, and tailored user profiles, the system supports seamless management of customer data, bookings, payments, and service feedback. Although the project was developed within a Salesforce Developer Edition for educational purposes, it closely mirrors real-world CRM implementation practices. This experience underscores the value of structured configuration, thorough testing, and scalable design, laying a strong foundation for future deployment and enhancements in live environments.

### Lesson Learned
Through working on the Tours and Travels Salesforce CRM project, I gained a clear understanding of how to build and structure a real-world CRM system using Salesforce. I learned the importance of starting with well-defined data models, setting up custom objects, configuring user access through profiles and roles, and automating processes using flows and triggers. Developing Lightning Web Components, writing Apex test classes, and using tools like the Data Import Wizard gave me valuable hands-on experience in building functional, user-friendly solutions.

One of the most important takeaways for me was the value of thorough testing. By preparing detailed test cases and validating flows, triggers, and reports, I ensured that every part of the system worked as intended. I also learned how crucial proper documentation and planning are for maintaining the system over time. Even though I didn't perform a live deployment due to Developer Org limitations, I now understand the deployment process in enterprise settings and feel more confident in applying these practices to future Salesforce projects.
	








