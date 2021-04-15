# G6EJD-ESP-File-Server
An ESP32 system that can perform a Directory, Upload, Download, Delete, Rename and Stream Files in SPIFFS

Using an ESP32 to handle file upload, download, delete, rename and streaming

Using the ESPAsynchWebserver and the SPIFFS filing system, with functions for:

Directory of SPIFFS files
Upload a file to SPIFFS
Download a file from SPIFFS to PC
Stream a file to PC browser
Rename a file in SPIFFS
Delete a file in SPIFFS
Display system information:
Upload and Download file size and transfer speeds
Filing system space and number of files
Processor system information
Network information
Setup Details

Download the two files to a folder
Ensure the listed libraries are included in your IDE
Click on the Credentials tab and edit the file accordingly:
If you do-not want accerss control then comment out the line #define AccessControl
If using access control: update the value for http_username and http_password .e.g. admin and admin
Update the logical server address name (if required) e.g. 'fileserver' or 'myserver'
Update the Wi-Fi Credentials to your own
Compile and upload
Access the server with http://fileserver/ or http://filserver.local
Or monitor the serial port and note the IP address then use your browser to connect to e.g. http://192.168.0.22/
Programme Notes:

It uses the ESP Asynchronous Webserver so there is nothing in the loop() section!

The webserver is event based, each event generates a response, there is no need to poll for client connections in the loop section

The loop section is free for your projects!

It is very fast!
