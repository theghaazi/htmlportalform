# AWS Arora Project

### Phase 1:
#### This Web Application
  - Can dynamically be changed to add more pages to the form.
  - Have a look and feel of a professional web application that can start services in the backend using API calls.
  - We will need this application to be a container that  can handle addition of pages and features.
  - This system can use DynamoDB in the backend.
  - Have the floating form feel to the open browser.
  - Should have a Federated authentication(AWS Cogneo; example in git has that integration) to manage users.
		  https://github.com/theghaazi/htmlportalform

    Tech to Use:
      1. html
      2. Node js or javascript (Client Side)
      3. html and associated file but separate .js under scr
      4. CSS
      ```
      root
        \scr
            index.js
            masterPage.js
        \style
            main.CSS
            other.CSS
            anythingelse.CSS
        \etc
        \instout
                  s3file_out_dateandtimestamped.JSON
                  s3file_out_dateandtimestamped.JSON
                  rdsfile_out_dateandtimestamped.JSON
                  rdsfile_out_dateandtimestamped.JSON
                  etc...
        \instin
                  s3file_in_dateandtimestamped.JSON
                  s3file_in_dateandtimestamped.JSON
                  rdsfile_in_dateandtimestamped.JSON
                  rdsfile_in_dateandtimestamped.JSON
                  etc...

        \index.html
        \masterPage.html
        \etc...
      ```




Key Deliverables
1. Login page that will connect to an authentication provider(Single Sign On):
    - Create a login screen that lets users log in or signup using AWS SSO authentication provided.
    - Login should timeout. The timeout setting should be adjustable utilizing an admin setting page.
    - Should have a placeholder for logs and text.
    - Able to disable authentication during testing/development
![Login-page with places to save image and text and disclamers](img/login-page.png)

	Login page that will connect to an authentication provider(Single Sign On):
	1	Create a login screen that lets users log in or signup using AWS Cogneto ( I will create a user pool and give you details ) SSO authentication provided.
	2	Login should timeout. The timeout setting should be adjustable utilizing an admin setting page.
	3	Should have a placeholder for logo and text(Footer, header read from a file).
	4	Able to disable authentication during testing/development 
	5	Every page in the web site should check for timeout and login before giving access to the page content.


	Main Landing page layout
	1	The landing page should be divided into section. So that each section can be either global(header, logo, footer, etc.)
		https://github.com/theghaazi/htmlportalform/blob/master/img/Sys-Diagram-MasterPageLayout.png
	2	Landing Page will have iPhone and Android like icons on it with should appear to be 3D (Shadow) these Icons can be images.
	3	The icons can be added by users and link them to html pages.
		https://github.com/theghaazi/htmlportalform/blob/master/img/Sys-Diagram-Master-Landing.png
	4	When Icons are clicked a "floating form or page should appear that the user can fill and interact. This form will have all the input field and tabs.
		https://github.com/theghaazi/htmlportalform/blob/master/img/Sys-Diagram-Landing-Admin.png

    2. A way to create icons on the landing page;
        - When users click the icones; this will open forms.
        - The icones will be circuler or iPhone/Android-like icons.
        - An settings page with form that will let me add icons to the landing page and
          1. link it to a form/Page.
          2. select a image of the icone.
          3. Setting to either open a form or take user to another html page.
          4. Some backgroud color and format.

    ![MainPage Layout](img/Sys-Digram-MasterPageLayout.png)
    ![Icones on Landing Page](img/Sys-Digram-Master-Landing.png)
    ![When click a button](img/Sys-Digram-Landing-Admin.png)

	Ability to scale up the web application
	1	The web app should be scalable. By that I mean, I (admin) should be able to add more html pages later and create icons on the landing page and link the icons to html pages.
	2	We already have a backend that we trigger from Linux. We need you to build a front end so user can view and interact with the backed.


3. A form that can write json to a new file in the root/ folder on the web page
  - Create a javascript form that can be filled with
    1. text
    2. radio buttons
    3. drop-down list
    4. multiline text area.
    5. submit button.
  - When save button is pressed data from the form is saved to a folder in the root "instout" in a JSON format with key as the field name and values as the input.

![feel like the menu is dropping down](img/image_1.png)
![feel like the menu is dropping down](img/image_7.png)
