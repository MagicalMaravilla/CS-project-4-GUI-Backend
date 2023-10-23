Home System Application Documentation
Overview
This document serves to explain the functionalities and features implemented in the Home System Application, a GUI-based application developed using Python and Tkinter. The application is designed to manage and control various aspects of a home security system, including door locks and auto-lock settings.

Frontend
SetupWindow
This window is the initial setup for a new user. It allows the user to create a username and password. The user must confirm the password before proceeding. If the user tries to exit the application during this setup, a confirmation dialog will appear.

LoginWindow
This window is displayed after the initial setup or when a user needs to log in. It requires the user to enter their username and password. If the credentials are incorrect, an error message is displayed.

AutoLockSetupWindow
This window allows the user to set up and manage the auto-lock feature. The user can set a specific time for the system to automatically engage the panic lock, or disable the auto-lock feature entirely.

HomeSystemApp
This is the main window of the application, providing access to various functionalities:

Panic Lock: Engages or disengages the panic lock, locking or unlocking all doors. If the panic lock is active, a password is required to deactivate it.
Door Control: Individual buttons for each door to lock or unlock them. These buttons are disabled if the panic lock is active.
User Settings: Allows the user to reset their username or password.
Logout: Logs the user out and returns to the LoginWindow.
Auto Lock Setup: Opens the AutoLockSetupWindow to manage auto-lock settings.
Disable Auto Lock: Disables the auto-lock feature and updates the status display.
The window also displays the current status of the panic lock, auto-lock settings, time until auto-lock (if enabled), and the status of each door.

Backend
HomeSystem
This class serves as the backend for the application, handling user authentication, door status management, panic lock functionality, and auto-lock settings. It also saves and loads user data and settings to and from disk.

Features Implemented
User Authentication: Secure login and setup using hashed passwords.
Door Status Management: Individual control of door locks, with the ability to save and load the status.
Panic Lock: A feature that locks all doors and requires a password to deactivate.
Auto Lock: Automatically engages the panic lock at a specified time.
User Settings Management: Allows the user to reset their username or password.
Persistent Data: User data, door statuses, and settings are saved to disk and loaded upon application start.
Error Handling: The application provides error messages for invalid inputs and actions.
Conclusion
This Home System Application provides a comprehensive and user-friendly interface for managing a home security system. The implementation of user authentication, door status management, and auto-lock features ensures a secure and efficient experience for the user.
