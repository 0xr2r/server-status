# POC server-status



##Server-Status leads to exposure information


# Introducing *server-status PWN*

server-status PWN constantly requests and parse Apache server-status page for any new event. Whenever a new URL is requested and a new client IP address is used, it will be logged and reported.

It outputs the data in a SQLITE3 database, and includes an option for saving unique URLs in a newline-delimited file.


## **Usage**

`python server-status.py u'http://example.com/server-status'`

#poc

![لقطة الشاشة 2026-01-14 093815](https://github.com/user-attachments/assets/695c5e07-4800-4bcb-a7d9-3a3adb4f0ed0)



The server-status page can be found on apache servers by making a GET request to /server-status. This will display some details about the server and a long list of requests made to the server and shown below
https://github.com/mazen160/server-status_PWN
python server-status_PWN.py — url ‘https://xxxx.com/server-status'
/server-status page for new requests and clients. If you let the tool run for a few hours or days you just might capture some sensitive information.
If the /server-status is exposed to the public then there is something wrong. This page can be used to monitor users GET requests for sensitive information. 
If the applications sends CSRF tokens, API keys, or anything else in a GET request then attackers will be able to see it. Using the server-status_PWN tool 
you can constantly monitor the page and examine the results later.

#poc

https://www.youtube.com/watch?v=vnPQ4ldKYds




