# Workbook Assignment A
### Patrick Hamer

### Q1 Describe the architecture of a typical Flask application: 200-300
<!-- The architecture of a web app describes the elements that make that app work and how they interact together. In our online library we should mention how we are using the MVC pattern, and how main file, controllers, models, schemas, etc. work together to show the required information (that is stored in a database) in JSON format.
A web app has an additional view layer, so the user interacts with the app through a website that renders the information in html pages -->
### Q2 Identify a database management system (DBMS) commonly used in web applications (including Flask) and discuss the pros and cons of this database150-250
PostgreSQL is an open source, object relational DBMS that has been around for decades and is the go-to for many industry professionals. It is operated through bash and while it has an amazing following it also has its limitations.
For a start, the fact that it is open source makes this a very cost effective way to do business, as well as making it possible to tailor it to your specific business needs. The downside of this is that without any one company owning it, it may be user friendly and commonly used it lacks the marketing budget to make it ubiquitous as well as not having as many skilled profesionals available for support.
It DOES support.
It is comparitively slower than some other DBMS (such as MySQ), however it DOES have increased integerity due to iuts ACID (Atomicity, Consistency, Isolation, and Durability) compliance. PostgreSQL is considered one of the most stable, secure DBMS in the market at the moment.
When it comes to scalability PostgreSQL talks a big game and has pretty extreme limits on the size of databases (32TB), however after reading some reviews it would appear that horizontal scaling can be a bit complex when it comes to setting up and managing.
While using PostgreSQL is fairly straightforward, and the use of write-ahead logging (WAL) makes it a fairly fault tolernat system, intitial install and setup can be a challenge for inexperienced users.
With all that being said there is a reason that PostgreSQL has been awarded "Database System of the year" a few times.
It is capable, stable, secure, efficient, and fairly intuitive to use.
### Q3 Discuss the implementation of Agile project management methodology
Agile project management is a more adaptive and efficient form of project management. Whereas in the past the recipe for a sellable product went in a direct line from conception to release the Agile methodology relies on a more flexible, iterative approach. Agile uses the **SCRUM** methodology, a set of protocols and processes that are used to continuously improve on problems as well as encourage collaboration.
From the beginning we start with Conception. As opposed to waterfall project management, Agile takes into account the user's story so they can truly grasp the goal of what they are designing.
The work in Agile is generally divided up into smaller tasks. This is to allow for a shorter feedback loop which drastically increases adaptability. These smaller tasks are often divided up using Kanban, which is a public list of which tasks are completed, need to be completed, need to be tested and finalized, who is working on them and how long (roughly) they are expected to take.
Initially a strategy meeting should be held so that tasks can be prioritized and assigned, as well as have estimated completion times and agreed 'Definition of Done' (DoD). These are all loose to allow for adaptability.
**Sprints** are one of the core principles of Agile. Sprints are a coordinated brief but intense period of the entire team working to achieve the same DoD. The big difference here is that the team is working in a smaller timeframe on a much more limited set of outcomes. Throughout the sprints daily *standups* should take place, allowing each worker to discuss what they are working on, any issues they may be having, what's next, what's done. This allows for transparency, acocuntability, and most importantly collaboration between colleagues.
After a sprint a retrospective should take place. This allows teams to discuss what worked, what didn't, what could be done better etc. This is also a good time to discuss and plan out the next sprint.
This approach to project management allows for a continuous, adaptive output of solid, shippable product to the consumer. The iterative process means that every time the customer recieves the product they can provide feedback, thus allowing for a development team better able to react to changing requirements.

### Q4 Provide an overview and description of a standard source control workflow
Source control is a way of coordinating the work of multiple developers, allowing them to have their own copies of working code while still maintaining a 'true' version as a source. It keeps a running history of changes to code and alerts users to conflicts when modifying, preventing accidental overwrites. An ancillary benefit of SCM is that it provides clear communication as to who is working at what when one users look at the history of the files.
Git workflow is comprised of these main features:
- **Repositories** are where the code is stored. Repositories can have multiple folders and files within them and like individual files a record of incremental changes will be kept.
- **Branches** are where a developer "branched" away form the source to work on new code. This allows them to work on and test new code in a way that will not effect the original source code.
- **Git commit** is like a snapshot of the work you are doing. A git commit should be performed often and always with a clear explanation so other developers can see what is happening.
- **Merging** is when updated files are merged from the staging area (git commit) and pushed to the source code. Saved to a new branch the incremental changes will be noted and should any conflicts occur they should be easily identified/located.
- **Conflicts** occur when two or more developers make changes to the same code, or when one person deletes a file while another edits it. Conlficts are highlighted by Git so as to be amended by the user.

### Q5 Provide an overview and description of a standard software testing process (e.g. manual testing) 100-200
**Manual Testing** is the process of having a human test software for bugs. It is an absolute necessity as no testing can be 100% automated and it also tests for one of the most important variables, user experience.  To perform manual testing one must understand the requirements of the software and create a clear test plan. Then after writing test cases to measure efficiency of all requirements and having them approved by a senior staff member, tests can be executed. If any of the software does not perform as expected then this will be considered a 'bug' and reported to developers. Within the umbrello of manual testing, in order of complexity (and often testing itself) there is:
**Unit testing**: The smallest testable individual componenets of software.
**Integration testing** Multiple *integrated* units tested as a whole to check operability.
**System testing** tests the combination of *all* integrated units for efficiency and, importantly, to make sure they meet the requirements of the software.
**UI testing** tests all the user interface aspects of the software, from font colour to menus. This is a very broad area.
**Alpha testing** is when the software is unleashed on actual people either internally or externally to test its appropriateness and effectiveness in the real world. This is where things like accesibility will be tested.

### Q6 Discuss and analyse requirements related to information system security and how they relate to the project
**Confidentiality**, or the notion that data could only be accessed by authorised users would be integral here. If users are having their personal details (CCard, home address etc) stored in a database you are managing then that information must be stored safely and securely. This could be achieved with an authentication process when using the app, keeping the data encrypted until users had varified their identity. While this would be approachable and user-friendly the downside is that the data WOULD be stored at your end, and would rely on the user being able to authenticate themselves.
**Accessibility** is the idea that data is accessible at all times to authorised users. This means that data should have some sort of backup process that in the event of a catastrophic failure data can still be accessed.
**Integrity**. That the data should bnot be corrupted is of the utmost importance. There are two times when data can be corrupted: when entered or while stored. This again comes back to authentication and authorisation but also toches on ideas like encryption, which would keep the data stored securely while it is not in use, also making it unusable if any unauthorised persons got hold of it. 
On top of all of this there must be clear lines of communication re: what is to be secured, how secure it is to be and how this will be done. Data security does not end at the PC and staff should be trained in the implementation of chosen security protocols. 



### Q7 Discuss common methods of protecting information and data and how you would apply them to the project
**Authentication**:  Using passwords and/or biometric data to authenticate who a user is will allow for sensitive information such as credit card details, home address, etc to be stored in a database linked to the user. This will make sure that the user is who they say they are and coupled with **authorization** should be used to protect their data. The Authorization of each individual will allow only them to see/edit their details within the system including payment information, personal details and even the password used for authentication. **Confidentiality** can be maintained with the use of automatically generated passwords.
The downside of this is that if a set of cirumstances arise where the user has lost/forgotten their password and has not authorized secondary account then the information could be lost, so perhaps having some sort of **physical security** such as a Government approved ID on file would in this case help solve the problem.
**Encryption** along with Authentication would significantly increase security. Not only would the data be unusuable if it were accessed, but also it would be impossible to decipher what data was actually being accessed in the first place.
**Destruction** of redundant sensitive information would also increase the confidentiality aspect of security. Once a user leaves (eg. unsubscribes) from the app, destroying their data would ensure that it could not be accessed by unaothorised persons.
**Access control** of staff is also imperative. Making sure that only appropriate people can access the data would minimise leaks and opportunities for both malicious people AND software. Something as simple as a Captcha could decrease bot accessibility while ensuring only relevant staff are authorised to sensitive information would minimise the potential for damage.
Finally keeping some sort of **backup** whether it be on a cloud or a remote server would ensure that in the case of a disaster the information would still be accessible.

### Q8 Research what your legal obligations are in relation to handling user data and how they can be met for the project
Schedule 1 of the Privacy and Data Protection Act 2014 (Vic) contains the Information Privacy Principles (IPPs). This is the bare minimum required for businesses in the public sector and should be the lowest standard achieved by any organisation.
Confidentiality and annonymity are two very import aspects of the privacy act. User data must be kept confidential and where possible must not be linked to any unique identifiers. While this may seem impossible while using databases, The fact of the matter is that as long as a user knows their login details it would be possible to maintain a degree of this annonymity. Having two seperate databases, one used for the general purpose of the app and one used for accounts/infrastructure could be maintained, with only relevant staff able to access the information that identifies customers.
Confidentiality coud be achieved with a combination of authentication, authorisation and encryption as per the answers to earlier questions. Keeping information locked behind security gateways would stop unauthorized staff accessing it and encryption would make sure that even if hackers got it, the information they had would be unusable.
Another aspect of the IPP act is informed consent. That customers would know what kind of data was being collected and stored as well as who that data was being shared with. This could be achieved with disclaimers and disclosure agreements. I think in this instance transparency is probably the best safeguard, so being up fornt and discussing with customers, ensuring they understand what data is being collected, why and who it will be shared with is paramount.


### Q9 	Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.

### Q10 Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.

### Q11 Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.

### Q12 Conduct research into a web application (app) and answer the following parts:  a. List and describe the software used by the app.50-100 per part
- b. Describe the hardware used to host the app.
- c. Describe the interaction of technologies within the app
- d. Describe the way data is structured within the app
- e. Identify entities which must be tracked by the app
- f. Identify the relationships and associations between the entities you have identified in part (e)
- g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)

### References:
https://agilemanifesto.org/
https://hive.com/blog/what-is-agile-project-management-methodology/

https://www.browserstack.com/guide/manual-testing-tutorial Jash Unadkat, Technical Content Writer at BrowserStack - December 11, 2021

https://ovic.vic.gov.au/privacy/information-privacy-principles-full-text/
https://content.legislation.vic.gov.au/sites/default/files/2022-08/14-60aa028%20authorised.pdf

https://www.cybertec-postgresql.com/en/postgresql-overview/advantages-of-postgresql/
https://www.guru99.com/introduction-postgresql.html