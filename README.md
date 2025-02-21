# Submission Reminder App Setup

## Overview
The `create_environment.sh` script automates the setup of a directory structure for the **Submission Reminder App**. It prompts the user for their name and uses it to create a personalized project directory named `submission_reminder_{yourName}`. The script then generates essential subdirectories and files required for the application.

## Features
- Prompts user for their name
- Creates a structured environment for the application
- Generates necessary subdirectories and files

## Directory Structure
After running the script, the following directory structure will be created:
```
submission_reminder_{yourName}/
│
├── app/
│   ├── reminder.sh
│
├── modules/
│   ├── functions.sh
│
├── assets/
│   ├── submissions.txt
│
├── config/
│   ├── config.env
│
├── startup.sh (to be created manually)
```

## Setup Instructions
### 1. Clone the Repository (if applicable)
```sh
# Clone the repository
# git clone <repository_url>
# cd into the project directory
cd <repository_folder>
```

### 2. Make the Script Executable
Ensure the script has execution permissions:
```sh
chmod +x create_environment.sh
```

### 3. Run the Script
Execute the script to set up the project:
```sh
./create_environment.sh
```

### 4. Provide Your Name
The script will prompt:
```
Enter your name:
```
Enter your name, and the project folder will be created accordingly.

### 5. Verify the Created Environment
Check if the directory and necessary files have been created:
```sh
ls -R submission_reminder_{yourName}
```

### 6. Run the Application
Once the setup is complete, manually create `startup.sh`, then execute:
```sh
./submission_reminder_{yourName}/startup.sh
```

## Script Explanation
- **Prompts the user** for their name
- **Creates the project directory** using the input name
- **Generates subdirectories**: `app`, `modules`, `assets`, `config`
- **Creates files**: `reminder.sh`, `functions.sh`, `submissions.txt`, `config.env`
- **Provides a ready-to-use structure** for the submission reminder app

## Notes
- Ensure you have execution permissions for `startup.sh` before running:
```sh
chmod +x submission_reminder_{yourName}/startup.sh
```
- `startup.sh` should be implemented separately to launch the application.

Repository Structure
The repository contains the following files and directories:

create_environment.sh: Script to set up the application environment.
README.md: This file, containing instructions and project details.
submission_reminder_yourName/: Directory created by the setup script, containing:
app/reminder.sh: Main script for checking submissions.
modules/functions.sh: Helper functions for the app.
assets/submissions.txt: File containing student submission records.
config/config.env: Configuration file for assignment details.
startup.sh: Script to start the application.

Example Output
When you run the application, you will see output similar to the following:

Starting the reminder app...

Running the reminder script...
Assignment: Literature
Days remaining to submit: 2 days
--------------------------------------------
Checking submissions in ./assets/submissions.txt
Reminder: Chiazokam has not submitted the Literature assignment!

Customization
You can customize the app to suit your needs:

Add More Students: Edit the submissions.txt file to include additional student records.
Change Assignment Details: Update the config.env file to modify the assignment name and deadline.
Extend Functionality: Modify the reminder.sh and functions.sh scripts to add new features.

## Author
Chukwuemeka Onugha.

## License
This project is licensed under the MIT License.

