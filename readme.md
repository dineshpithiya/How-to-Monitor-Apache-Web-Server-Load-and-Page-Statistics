# How to Monitor Apache Web Server Load and Page Statistics

> Today we are here with another article on the Apache HTTP web server which can make a System Administrators life much easier to handle load of Apache web server using mod_status module.

## What is mod_status?

> mod_status is an Apache module which helps to monitor web server load and current httpd connections with an HTML interface which can be accessible via a web browser.

> Apache’s mod_status shows a plain HTML page containing the information about current statistics of web server state including.

1. Total number of incoming requests
1. Total number of bytes and counts server
1. CPU usage of Web server
1. Server Load
1. Server Uptime
1. Total Traffic
1. Total number of idle workers
1. PIDs with respective client and many more.
1. The default Apache Project enabled their server statistics page to the general public. To have a demo of busy web site’s status page, visit.

```
URL:- http://www.apache.org/server-status
```
> Enable mod_status in Apache
> Configure mod_status into your vertual host
Make sure
```
<Location /server-status>
	SetHandler server-status
	Order allow,deny
	Deny from all
	Allow from example.com 
</Location>
</VirtualHost>
```
> Enable ExtendedStatus
> Restart Apache

Now run Your URL Like:- http://serev-hostname/server-status and it will return out out same like below SS

![GitHub Logo](/mod_status-620x420.jpeg)
