# Surfer: Walkthrough

## Introduction:

"Surfer" provides an opportunity to refine your SSRF (Server Side Request Forgery) attack skills.

Explore the room on TryHackMe: [Surfer Room](https://tryhackme.com/room/surfer)

## Understanding SSRF:

SSRF, an acronym for Server Side Request Forgery, represents a critical vulnerability that empowers attackers to manipulate web applications, thereby facilitating unintended connections to specific locations.

## Commencement

Our journey begins with the pursuit of valuable insights, with the room hinting at the existence of functionality designed for internal use.

## Mission Brief

Uncovering Hidden Functionality
Overcoming Access Control Mechanisms
Progressing Further

Our investigation proceeds with a meticulous Nmap scan of the web application. Employing a thorough approach with the '-T4' aggressive option, we focus on scanning the top 1024 ports. Our rationale for this choice is rooted in the belief that there may not be any noteworthy ports beyond this range.

```bash
nmap TargetIP -top-ports=1024 -T4
```

The results indicate that only two ports are active. With this information in hand, we continue to the next phase of our exploration.

## Exploration of Content and Directory Structure

We opt for the DirBuster tool by OWASP, supplementing our efforts with a medium-sized wordlist located at '/usr/share/dirbuster/wordlists/'. Our objective is to systematically investigate text files, revealing two accessible files of significance:

**/changelog.txt**: This file houses a log documenting notable changes within the application.
**/robots.txt**: Contained within is a reference to a page, '/backup/chat.txt', which is flagged as unsuitable for crawling.

## Investigation of '/backup/chat.txt'

Our attention turns to the contents of '/backup/chat.txt', which reveals an exchange of messages between the system administrator and the developer, Kate. Of particular note is a directive from Kate:

```bash Kate: Additionally, please remember to update your credentials. Avoid using your username as your password. ```

## Authentication Attempt

Guided by Kate's advice, we proceed to authenticate with the provided credentials, aligning the username and password in accordance with her directive.

Successful Authentication Achieved

## Navigation Through the Application

As we explore the application further, we encounter a notable feature – the 'Export PDF' option, a subject of prior discussion between Kate and the system administrator.

Moreover, we identify an internal page situated at '/internal/admin.php'. However, an attempt to access this page is met with a restriction, permitting solely local access (from '127.0.0.1').

## Request Interception with Burp Suite

To progress, we employ Burp Suite to intercept the request responsible for generating PDFs. This request features a crucial parameter named 'url', specifying the URL of the PDF hosted on the same server. We forward this request to the repeater for in-depth analysis.

The PDF report received informs us that it is generated for the same server that initiated the request, effectively pointing to "localhost."

### Operating Mechanism:

User triggers the export PDF function.
The frontend initiates a POST request, including the URL, to the server.
The server forwards a request to the specified URL and subsequently receives and transmits the response to the frontend.
At this juncture, we contemplate the possibility of crafting a POST request capable of compelling the server to request a page available locally (on the same server).

## Exploitation and Flag Retrieval

Implementing a strategic maneuver, we substitute '/server-info.php' with '/internal/admin.php'. This alteration effectively induces the server to initiate a request to '/internal/admin.php' within its local environment, culminating in the retrieval of the coveted flag within the server's response.

Objective Accomplished: The Flag is Secured

## Closing Remarks

We trust that this walkthrough has equipped you with valuable insights and knowledge. Should you have any questions or seek further clarifications, we encourage you to utilize the comment section. We also invite you to share this knowledge within the information security community, and we look forward to your continued support.

Sincerely,

[Your Name]

Please replace [Your Name] with your name or desired authorship attribution. This refined content can be readily utilized on GitHub or in any professional documentation.
