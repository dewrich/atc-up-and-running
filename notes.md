## NOTES

## Components Reminder: WHAT'S IT WRITTEN IN?

* Welcome to Traffic Control - Up and Running
  * Ask questions in our slack channel
  * Introduce Dan Kirkwood and his role
    * Point out how new the Docker version of CIAB is
* Give a high level overview of the breakdown of the presentation

* Summarize verbally at the end


* ADMIN_DOWN: Temporary down. Edge: XMPP client will send status OFFLINE to TR, otherwise similar to REPORTED. Mid: Server will not be included in parent.config files for its edge caches
* CCR_IGNORE: Edge: 12M will not include caches in this state in TR config files. Mid: N\/A for now
* OFFLINE : Edge: Puts server in TR config file in this state, but TR will never route traffic to it. Mid: Server will not be included in parent.config files for its edge caches
* ONLINE: Edge: Puts server in TR config file in this state, and TR will always route traffic to it. Mid: Server will be included in parent.config files for its edges
* REPORTED: Edge: Puts server in TR config file in this state, and TR will adhere to the health protocol. Mid: N\/A for now

Resources: 

Note: a rehearsal usually will run about 20% shorter than a live presentation; adjust your content accordingly.

[https://www.washington.edu/doit/presentation-tips-0](Presentation Tips)

[5 Ways to make the audience the star](https://www.fastcompany.com/3041558/5-ways-to-make-the-audience-the-star-of-your-presentation)

[Useful English Phrases for a Preso](https://www.topcorrect.com/blog/useful-english-phrases-for-a-presentation)
