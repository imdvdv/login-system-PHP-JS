# PHP Login System

### Project Overview

This project is a registration, login and personal profile management system. The backend of the project is written in PHP, and the frontend in Javascript.
The main goal of the project is to learn how to implement such functionality and understand how they work without using frameworks and third-party libraries.

### Features

* __Registration:__ Users can register by providing a username, password, and email address.
* __Login:__ Registered users can log in using their username and password.
* __Remember Me:__ Users can visit his profile after terminating the session and closing the browser without re-entering the password using cookies.
* __Password recovery:__ Users can reset their password if they forget it by providing their email address. Delivery of letters for convenience and reliability is implemented using the PHPMailer library
* __Profile editing:__ Users can edit their profile information, including their username, email address, and profile picture or delete own profile.
* __Logout:__ Users can log out of their session and delete cookies if they exist.
* __Validation:__ The project implements a custom validation of input data before sending using JavaScript and additional validation on the server side. In case of errors, error messages are displayed each under its own field.
* __Popup:__ The project implements a custom popup for displaying messages or forms that the function retrieves using fetch JS from the components directory.

### Components

__Languages__
* PHP-8.2.4
* JavaScript
* MariaDB-10.4.28
* HTML5
* CSS3

__External Resources/Plugins__
* PHPMailer-6.9.1
* Font awesome-6.4.0
* Google Fonts

### Getting Started

To use this project, follow these steps:
1. Clone the repository to your local machine.
2. Configure Database.

   2.1 Create a new database with name `login_system` and import the prepared dump file `src/config/login_system.sql`.
   
   2.2 Edit the database connection details in the `src/config/env.php` file.

   ```php
      // Database params
      const DB_HOST = "your DB Host", 
          DB_NAME = "your DB Name", // "login_system" if you decide to use the database dump attached to the project
          DB_USERNAME = "your DB UserName", 
          DB_PASSWORD = "your DB Password", 
          DB_PORT = "your DB Port",
          DB_CHARSET = "utf8",
          DB_OPTIONS = [PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC];
   ```
3. Configure email sending using [PHPMailer](https://github.com/PHPMailer/PHPMailer).

    3.1 Install [composer](https://getcomposer.org/) if it is not available in your development environment

    3.2 Edit the PHPMailer params in the `src/config/env.php` file. 
    ```php
       // PHPMailer params
       const MAIL_HOST = "your SMTP host",
           MAIL_USERNAME = "your SMTP username", // your email address
           MAIL_PASSWORD = "your SMTP password",
           MAIL_PORT = "your SMTP port",
           MAIL_CHARSET = "UTF-8",
           MAIL_DEBUG = 0; // more details in the documentation for PHPMailer
   ```
    3.3 Enter YOUR DOMAIN name or localhost into the message variable in the `src/actions/access-recovery.php` file.
    ```php
      $message = 'To reset a password and create new - <a href="http://{YOUR_DOMAIN}/pages/change-password.php?code='.$code.'">click here</a>. </br>Reset your password in a hour.';
    ```

4. Run the project on a server.

### Images

![Login page](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/login-page.png)
![Signup page](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/signup-page.png)
![Signup page with errors](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/signup-page-errors.png)
![Access recovery page](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/access-recovery-page.png)
![Change password page](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/change-password-page.png)
![Profile page](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page.png)
![Avatar dropdown1](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page-avatar1.png)
![Avatar popup](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page-avatar2.png)
![Avatar dropdown2](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page-avatar3.png) 
![Change password popup](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page-password-popup.png)
![Delete profile popup](https://github.com/imdvdv/PHP-JS-Login-system/blob/master/assets/img/profile-page-delete-popup.png)
