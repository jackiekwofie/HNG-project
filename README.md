# HNG-project 
# User Management Script
Overview
This repository contains a Bash script for managing user creation on Linux systems. The script reads a list of usernames and optionally groups from an input file, creates users, assigns them to personal groups, sets passwords, and logs actions.

# Features
Creates users and their personal groups.
Sets random passwords for new users.
Logs user creation actions to /var/log/user_management.log.
Stores usernames and passwords securely in /var/secure/user_passwords.csv.
# Prerequisites
Linux operating system (tested on Ubuntu).
Bash shell (/bin/bash).
OpenSSL for password generation (openssl).
Root privileges (sudo).
# Usage
Clone the repository

# Create a text file (user_list.txt for example) with each line formatted as username;group.
Example:
alice;admin
bob;users
charlie;
Run the script:

# Ensure the script is executable:
chmod +x create_users.sh
Execute with sudo (root privileges required):
sudo ./create_users.sh user_list.txt
View logs and passwords:

# Log file (/var/log/user_management.log):
sudo cat /var/log/user_management.log
Passwords file (/var/secure/user_passwords.csv):
sudo cat /var/secure/user_passwords.csv
Notes
Ensure the input file (user_list.txt) is correctly formatted with usernames and groups separated by a semicolon (;).
Existing users are skipped during execution to prevent duplicates.
The script requires root privileges to create users and modify system files
