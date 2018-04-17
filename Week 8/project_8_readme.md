# Project 8 - Pentesting Live Targets

Time spent: **around 3.5** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1:  SQL Injection (SQLI)
After "php?id=", if you put ' OR SLEEP(5)=0--', then the page would take 5 seconds until it fully loads, telling us that the sql injectoin has worked

Vulnerability #2:  Session Hijacking/Fixation
In Chrome, I logged into the site and copied the sessoin ID. After that, I opened Safari and open the same webpage without logging in. I changed the session ID of the web page in Safari, to the one from Chrome, and it automatically logged me in, without having to put in useranme and password. 


## Green

Vulnerability #1: Cross-Site Scripting (XSS)
After putting the XSS in the feedback, when a registered or admin user opens it, it produces an alert 

Vulnerability #2: User Enumeration
If you put jaecho as an username, it produces error saying that the log in was unsuccessful. However, if you put a jmonroe99, which is an existing username in the system, it produces a bold error with the same message, telling us that this username exists.


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
When logged in, we can see that Lazy Lazyman was fired for stealing, thus not showing up to the public site. However, since Lazy Lazymnas ID was 11, we can see his data when we put in 11 after the ID in the web address. This does not work on the other sites, such as blue site.

Vulnerability #2: Cross-Site Request Forgery (CSRF)
After sending a feedback telling them to visit certain link, it has a hidden form that will change the Ken Barker's information.


## Notes
It took a bit to get it started since I didn't know to where to start. It took some trial and errors for some of them. The hints page on the codepath site helped a lot. Also, I didn't really know how to use the GIF thing, so I took screenshots instead. I hope I included enough pictures.
