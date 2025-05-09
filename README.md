## Overview

Welcome to the **FTP Scanner**, a tool designed for cybersecurity professionals and enthusiasts involved in Capture the Flag (CTF) competitions and pentesting activities. This script helps you identify anonymous FTP logins, lists files, grabs banners, and checks for known vulnerabilities against a database.

## Features

- **Anonymous Login Detection**: Checks if an FTP server allows anonymous logins.
- **File Listing**: Lists all files available in the FTP directory.
- **Banner Grabbing**: Extracts the FTP server banner.
- **Vulnerability Scanning**: Compares the extracted banner against a local database of known vulnerabilities.


Make sure you have Python 3.8+ installed. You'll also need to install the required dependencies:
## Setup
```sh
sudo apt install python3-venv

python3 -m venv venv
source venv/bin/activate
cd venv

git clone https://github.com/MIISTERC/ftp-scan.git
cd ftp-scan
sudo bash setup.sh
```
You can use the automated setup file `setup.sh` or you can do it manually..
```sh
git clone https://github.com/MIISTERC/ftp-scan.git
cd ftp-scan
pip3 install -r requirements.txt
sudo ln -s <path>/ftp-scan/ftpscan.py /usr/bin/ftpscan
ftpscan -h
```
or you can just use it by
```sh
python3 ftpscan.py -h
```
## Usage
```sh
ftpscan -t 127.0.0.1 (default port is 21)
ftpscan -t 127.0.0.1 -p 1234
```
## Warning
1.Make sure the shebang in `ftpscan.py` matches your actual python3 path if it does , then you are good to go :)
<br>
2.After running setup.sh , please don't move the script to another location as it deflects the symbolic link and as well as the script cant open the `.db` file. instead after cloning leave the `ftp-scan` directory as it is.
## output
Example output
<br>
![output](https://github.com/user-attachments/assets/f46cd135-b17e-4bd1-a350-07214efd6291)


hope this tools! Help you..

