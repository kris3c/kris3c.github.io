# Decoding TBHM 2 x001 : Enlightening the Sword

![1](https://github.com/kris3c/kris3c.github.io/assets/128035061/f6529d46-099d-40bc-a4d6-21b5d3c6d1b4)

Hey there, hackers! Welcome to the hackeries series, 'Decoding The Bug Hunter Methodology 2.' I'm excited to share everything I learned from TBHM2, an amazing class led by the legendary hacker, [Jason Haddix](https://twitter.com/Jhaddix). Big thanks to Jason for letting me join in and discover these incredible gems of knowledge. Trust me, being part of TBHM2 feels like winning the jackpot!

Throughout this series, I'll break down TBHM2 into five easy-to-digest articles. If you're eager to dive into Jason Haddix's treasure trove of knowledge, stick around and follow along from the beginning. You won't want to miss it!

Let's Begin the Journey

### Table of Content

- [Catching the Target](#catching-the-target)
- [Sharping the Report](#sharping-the-report)
	- [Template by the OG Haddix](#template-by-the-og-haddix)
- [Crafting a Notebook](#crafting-a-notebook)
	- [Mapping the Target](#mapping-the-target)
- [Connect with Me](#connect-with-me)

## Catching the Target

Firstly, before doing anything else we should have a target in our bag and understanding how to choose the target is a most required skill. 

There are mainly three types of Bug bounty Programs : 

- Self hosted 
- Embedded Forms 
- Hosted on Bug Bounty platforms 

For discovering the Self hosted and Embedded Form BB programs we can use Google Dorks those who don't know about google dorking they can refer to [Friendship with Google : Dorks](https://kris3c.github.io/article/Friendship-with-Google-Dorks) .

Words from Haddix : When searching for BB programs on BB platforms you should remember "World is wider then two" means there are not only 2 platforms in the world hackerone and bugcrowd there are many good platform that Strongly needed to be added in your review list. Some of the Suggested platforms are : 

- Synack 
- zerocopter
- hackenproof
- detectify
- yogosha
- BugBounty.jp
- cobalt
- immunefi 
- bugv
- Yes We Hack
- Intigriti

*For Bug Hunter*  

- When selecting the BB Program you should carefully read the scope and policy section of the program and search for the "catch all" statement. Catch all means the program is allowing you to report the issues in the service or sites that belongs to the target company but not specified in the target list.

*For Red Teamers*

- In red team engagement you should push for objective based testing.

## Sharping the Report 

The most important thing to note is that the report should contain more defensive information rather than the information about the actual attack. keep the ratio 70:30 because the IT department of the company is more interested in how they can implement the defensive mechanism to prevent the vulnerability that you have discovered.

**Fact :** Better documentation can sometimes gives an strong reason to the company to pay even for the duplicate.
### Template by the OG Haddix 

*In each of the section Include only the necessary information just digging and adding fillers to the section will decrease the chances of begin accepted.**

**Technical Issue - [vulnerability name]**

- This Section should include all the crucial information related to the affected part of the web application.
- Also include the payload you have used to verify the vulnerability.

**Reproduction** 

- Include all the step required to reproduce the issue.
- Each Step follow a sequence and should be clear and short.

**Impact**

- What are the impacts and why they are valid?
- Adding Impact in the discovered context will have a great impact on triager.

**Developer and Remediation Notes**

- Remember this tips are for the developers not for the triager so think from the developer perspective.
- Tips should be detailed and specific.

**Reference**

- Include some resources as a reference to the discovered vulnerability.

## Crafting a Notebook 

Tracking the process is a must step for every pertest as it keeps you updated about how much you have been reached the surface area of the target.

Some of the best Hierarchical based note taking applications :

- [OneNote](https://www.onenote.com/download)
- [Cherrytree](https://redirect.viglink.com/?format=go&jsonp=vglnk_170144436748110&key=eac202ea7a96cf485281d6c4ffa2069e&libId=lpms1m040103es17000ULc932ia65&loc=https%3A%2F%2Fwww.makeuseof.com%2Ftag%2Fproductivity-on-linux-7-apps-for-note-taking%2F&v=1&opt=true&optExText=false&out=https%3A%2F%2Fflathub.org%2Fapps%2Fnet.cozic.joplin_desktop&ref=https%3A%2F%2Fwww.google.com%2F&title=The%20Top%2010%20Note-Taking%20Apps%20for%20Linux&txt=Joplin)
- [EverNote](https://evernote.com/download)
- [Simple Note](https://redirect.viglink.com/?format=go&jsonp=vglnk_170144442217611&key=eac202ea7a96cf485281d6c4ffa2069e&libId=lpms1m040103es17000ULc932ia65&loc=https%3A%2F%2Fwww.makeuseof.com%2Ftag%2Fproductivity-on-linux-7-apps-for-note-taking%2F&v=1&opt=true&optExText=false&out=https%3A%2F%2Fflathub.org%2Fapps%2Fcom.simplenote.Simplenote&ref=https%3A%2F%2Fwww.google.com%2F&title=The%20Top%2010%20Note-Taking%20Apps%20for%20Linux&txt=Simplenote)
- [Joplin](https://joplinapp.org/help/install/)

When Working in a team we can also use [Google Spread sheet](https://workspace.google.com/intl/en/features/?utm_source=sheetsforwork&utm_medium=et&utm_content=trysheetsforwork&utm_campaign=hero) for storing the information as it allows us to easily share the progress within the team.

### Mapping the Target

As everybody knows visualising any information makes it more easy to manage. Creating mind maps for the target assets can help us to keep track of the progress in more effective and efficient manner.

Some of the best mind mapping applications :

- [Xmind](https://xmind.app/) - Jasson's Preferred Application
- [coggle](https://coggle.it/)
- [gitmind](https://gitmind.com/)

This wraps up the x001 part of this series. In the upcoming x002 part, we'll dive into the complete reconnaissance methodology. Stay [KriTuned](https://kris3c.github.io/kritune/) for more insightful exploration!

## Connect with Me:

Follow me on these platforms to stay updated and engage in the ADventure:

- [Twitter](https://twitter.com/Krish_Ars3)
- [LinkedIn](https://www.linkedin.com/in/kris3c/)

Your questions, feedback, and insights are always valued as we navigate this educational odyssey.

<script src="https://utteranc.es/client.js"
        repo="kris3c/kris3c.github.io"
        issue-term="pathname"
        label="KriCom"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>















