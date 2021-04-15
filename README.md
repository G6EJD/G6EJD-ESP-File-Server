# ESP-File-Server
An ESP32 system that can perform a Directory, Upload, Download, Delete, Rename and Stream Files in SPIFFS

Using an ESP32 to handle file upload, download, delete, rename and streaming

Using the ESPAsynchWebserver and the SPIFFS filing system, with functions for:
1. Directory of SPIFFS files
2. Upload a file to SPIFFS
3. Download a file from SPIFFS to PC
4. Stream a file to PC browser
5. Rename a file in SPIFFS
6. Delete a file in SPIFFS
7. Display system information:
    * Upload and Download file size and transfer speeds
    * Filing system space and number of files
    * Processor system information
    * Network information
    * Setup Details

SETUP Instructions

1. Download the two files to a folder
2. Ensure the listed libraries are included in your IDE
3. Click on the Credentials tab and edit the file accordingly:
4. If you do-not want accerss control then comment out the line #define AccessControl
5. If using access control: update the value for http_username and http_password .e.g. admin and admin
6. Update the logical server address name (if required) e.g. 'fileserver' or 'myserver'
7. Update the Wi-Fi Credentials to your own
8. Compile and upload

Access the server with http://fileserver/ or http://filserver.local

Or monitor the serial port and note the IP address then use your browser to connect to e.g. http://192.168.0.22/

Programme Notes:
1. It uses the ESP Asynchronous Webserver so there is nothing in the loop() section!
2. The webserver is event based (asynchronous), each event generates a response, there is no need to poll for client connections in the loop section
3. There are test files to try out uploading and download, etc
4. The loop section is free for your projects!

It is very fast!
