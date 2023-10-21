Surfer : Walkthrough
"Surfer" is a room that will help you to test your SSRF attack skill.
Tryhackme : https://tryhackme.com/room/surfer
SSRF : It stands for server side request forgery, It is a vulnerability that allow the attacker to induce webapplication to make connection to unintended location.
Starting : Looking for useful information
The room says there is a functionality for internal uses
Task
1. Finding the functionality
2. Bypassing access control
Going Forward
1. First we will run nmap scan against web application
I am scanning for top 1024 ports with aggressive option (-T4) beacuse i don't think there are intersting ports
nmap TargetIP - top-ports=1024 -T4
It says only two ports are open so moving on for next step
2. Discovering some content (Files and Directory bruteforcing)
I am using dirbuster by OWASP with its medium wordlist located at /usr/share/dirbuster/wordlists/ for bruteforcing txt files there is two accessible files
/changelog.txt : contain some log of changes in application
/robots.txt : contain a page /backup/chat.txt that should not be crawled
3. Going to /backup/chat.txt
chat.txt file contain chats between admin and developer kate
it have a intresting message from kate
Kate: Also Don't forget to change the creds, plz stop using your username as password.
4. Try to login with credentials
hint : think about the message from kate he says password is same as username what's the username
Succeed
5. walking through application
There is a export pdf option about which developer kate was talking with admin
There is a internal page hosted on /internal/admin.php but after visting it says can only be accessed locally (from 127.0.0.1)
6. Intercept with burp the request for pdf going to server
there is paramter url contating url of the pdf present on the same server
send it to the repeater
the pdf in the response says the report is for the same server who initiated the request (localhost).
mechanism :
User clicked on export pdf > frontend send a POST request containing a url to the server > server send a request to the submitted url and receive response > sending response to the frontend
What if we a POST request to the server that induce it to request a page available on same server (locally)
Exploiting :
Replace /server-info.php with /internal/admin.php
this will cause the server to request /internal/admin.php locally
Boom you got the flag in response submit the flag and enjoy
Last words
I hope you learned something from this article. If you have any type of query comment box is always open for you.
Don't forget to share this article with your friends to spread knowledge in infosec community.
Do follow to stay connected for more informative articles.
Thankyou, Happy Hunting
