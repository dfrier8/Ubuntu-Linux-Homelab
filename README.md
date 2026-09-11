# Ubuntu Linux Home Lab

## Project Overview
Built a dedicated Linux home lab using an older Lenovo laptop to gain hands-on experience with Linux system administration.

## Environment
- Ubuntu Linux
- Lenovo laptop
- Bootable USB installation media
- Rufus
- Bash terminal

## Phase 1 – Ubuntu Installation

### Installation Process
1. Downloaded the Ubuntu Desktop ISO.
2. Downloaded and launched Rufus on a Windows computer.
3. Connected an 8 GB USB flash drive.
4. Selected the Ubuntu ISO in Rufus.
5. Created the bootable USB using ISO Image Mode.
6. Restarted the Lenovo laptop and opened the boot manager.
7. Selected the USB flash drive as the boot device.
8. Booted into the Ubuntu installer.
9. Selected the interactive installation option.
10. Selected the default application installation.
11. Configured the disk to erase the existing operating system and install Ubuntu.
12. Selected the default file system configuration without encryption.
13. Created a local Ubuntu user account and computer name.
14. Completed the Ubuntu installation.
15. Restarted the laptop and booted into the installed Ubuntu operating system.

# Phase 2 – Command Line & File Management
After installing Ubuntu, I created an IT lab directory structure and practiced fundamental Linux command-line and file management tasks.

### IT Lab Structure
Created the following directories:

    backups
    documentation
    logs
    scripts
    users


### Commands Used

    pwd – Display the current working directory
    ls – List directory contents
    cd – Navigate between directories
    cd .. – Move to the parent directory
    mkdir – Create directories
    touch – Create files
    mv – Rename or move files
    cp – Copy files
    cat – Display file contents
    uname -a – Display Linux system information
    > – Redirect command output into a file


### System Information Documentation
Used uname -a to retrieve Linux system information and redirected the output into system-info.txt.

Verified the saved information using cat.

File Management Practice
Practiced creating, renaming, copying, and locating files across the IT lab directory structure using relative paths.
<img width="1358" height="760" alt="Directory Screenshot Phase 2" src="https://github.com/user-attachments/assets/d688b9eb-5332-49a3-85f0-a6a60d7efae8" />

## Phase 3 – Users & Groups
    In this phase, I practiced Linux user and group administration by creating user accounts, assigning passwords, creating a shared group, and managing group membership.

### User Account Creation
    Created two Linux user accounts with home directories using useradd and assigned passwords using passwd.

    Commands used:

    sudo useradd -m analyst1

    sudo useradd -m technician1

    sudo passwd analyst1

    sudo passwd technician1
<img width="1366" height="768" alt="technician analyst useradd -m" src="https://github.com/user-attachments/assets/5944fffa-79e9-484b-94db-ee63e2ec199e" />

    


### Group Creation and Membership
    Created the itteam group and added both users as members.

    Commands used:

    sudo groupadd itteam

    sudo usermod -aG itteam analyst1

    sudo usermod -aG itteam technician1

    Verified group membership using:

    grep itteam /etc/group
<img width="1366" height="768" alt="Groups created" src="https://github.com/user-attachments/assets/56e9e3f3-8972-441c-9103-53c990784543" />

    



### Managing Group Membership
    Practiced removing a user from a supplementary group and adding the user back.

    Commands used:

    sudo gpasswd -d technician1 itteam

    sudo usermod -aG itteam technician1

    I verified each change by checking the itteam entry in /etc/group.

   <img width="1366" height="768" alt="Group Management" src="https://github.com/user-attachments/assets/08598b28-199d-48bd-9445-d68e6e4ca5b2" />


### User and Group Verification
    Used the id command to verify each user's UID, primary GID, and supplementary group membership.

    Commands used:

    id analyst1

    id technician1

    Both accounts were successfully verified as members of the itteam group.

<img width="1366" height="768" alt="Final verification" src="https://github.com/user-attachments/assets/b94cd1a5-b7d5-4218-8ab3-01752e7cdc9b" />

