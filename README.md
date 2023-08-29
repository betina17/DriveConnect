## Overview

This application is designed for real-time communication and incident reporting between drivers. Developed in C++, the application leverages Object-Oriented Programming (OOP) principles to create a modular codebase. It features a layered architecture, separating the domain logic, data access, and user interface into distinct layers . The graphical user interface is built using the **Qt framework**, providing a user-friendly experience. The application employs the **Observer design pattern** to keep all instances in sync, particularly for real-time chat and report updates.

## Description

• The application reads information about all registered drivers from a text file at startup. Each Driver has a name (string), a current location (latitude and longitude), and a score.

• Another file contains road reports. Each Report includes a description, the reporter's name (the driver who reported it), the exact location (latitude and longitude), and a validation status (bool). The application reads these reports at startup.

• Upon launching the application, a new window is created for each driver. The title of the window is the driver's name, and the window also displays the driver's current location and score. The window shows all reports within the driver's region of interest, defined as a radius of 10 units from the driver's current location using the Euclidean distance. All report information is displayed, and valid reports appear in bold font.

• Each driver's window contains a real-time chat control, allowing all drivers to communicate. Messages sent by any driver are visible to all other drivers and are displayed alongside the sender drivers' names.

• Any driver can add a new report by inputting the description and exact location. The reporter is automatically set to the name of the driver who added the report.

• When a modification is made by any driver, it is automatically visible to all other drivers. The application uses the Observer design pattern for this functionality.

• When the application closes, the reports file is updated.



