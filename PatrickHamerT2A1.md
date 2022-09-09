# Workbook Assignment A
### Patrick Hamer

### Q1 Describe the architecture of a typical Flask application: 
A typical flask application, beginning from the user themselves would start at the User interface. This is called the *client layer*. This is essentially the user-end app that will be used to request and receive information, usually written in HTML, CSS and JS. The client layer will use HTTP requests to communicate with the app layer. For example a user may enter an address for a netflix movie. The GUI (Graphical User Interface) will communicate this to the *API layer*.
An API is basically software that allows different machines to communicate with one another. The API will forward instructions to the server's *app layer*, which is where to the logic required to perform requests will be stored. This will be written on Python, Ruby, Java or any other programming language. This is where the calculations will be performed to figure out exactly what it is the server side should be doing. For our example on Netlfix, the app layer will locate and retrieve the movie from the database layer.
Information will be retrieved from the *database layer*. This layer is where the the bulk of information is stored and where you will find applications like PostgreSQL in operation. It will the SQL that allows for data to be retreved according to the logic dictated by the app layer. This is also where you will find the files for things like video and audio for our netflix example. Databases are organised into tables that have identifying keys for each entity, thus making retrieval mroe efficient.
*3rd Party* layers are things such as Paypal, 'Login with facebook', Steam etc. These are 3rd party apps that can be linked to work in another app. In this instance it's actually a bit dodgy as Netflix has pulled some tricks in the past to avoid Apple's App Store fees, however what would normally happen is that external software wpould handle things like payment. Whether it be for security reasons, or simply because an app has become so commonly used as to be a means of identification in itself, this external party will usually have resources dedicated to some specific aspect that our app uses. For example PayPal would already have the infrastructure in place to handle sensitive information such as credit card details, as well as existing information pertaining to the individual customer thus making outsourcing this work more cost effective
Finally there is the *administrative layer*, which is the system that manages and polices the entire operation, for example setting/retrieving passwords, assigning authorisation levels for users and staff, etc. This would be why you and I cannot upload a movie to Netflix, and also why certain titles can be removed from the service if they are deemed inappropriate.


### Q2 Identify a database management system (DBMS) commonly used in web applications (including Flask) and discuss the pros and cons of this database
PostgreSQL is an open source, object relational DBMS that has been around for decades and is the go-to for many industry professionals. It is operated through bash and while it is a fantastic piece of software it also has its limitations.
For a start, the fact that it is open source makes this a very cost effective way to do business, as well as making it possible to tailor it to your specific business needs. The downside of this is that without any one company owning it, it may be user friendly and commonly used it lacks the marketing budget to make it ubiquitous as well as not having as many skilled profesionals available for support.
It is comparitively slower than some other DBMS (such as MySQL), however it DOES have increased integerity due to its ACID (Atomicity, Consistency, Isolation, and Durability) compliance. PostgreSQL is considered one of the most stable, secure DBMS in the market at the moment. It is also often going to be slower than NoSQL databases as it may have to run through many joined tables to answer a query, whereas in NoSQL tables are optimised for such actions.
When it comes to scalability PostgreSQL talks a big game and has pretty extreme limits on the size of databases (32TB), however after reading some reviews it would appear that horizontal scaling can be a bit complex when it comes to setting up and managing. This is a contrast to something like NoSQL, where horiontal scaling is not an issue.
While using PostgreSQL is fairly straightforward, and the use of write-ahead logging (WAL) makes it a fairly fault tolerant system, intitial install and setup can be a challenge for inexperienced users.
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
**Confidentiality**, or the notion that data could only be accessed by authorised users would be integral here. If users are having their personal details (Credit Card, home address etc) stored in a database you are managing then that information must be stored safely and securely. This could be achieved with an authentication process when using the app, keeping the data encrypted until users had varified their identity. While this would be approachable and user-friendly the downside is that the data WOULD be stored at your end, and would rely on the user being able to authenticate themselves.
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
From a broader perspective, given that customers may not reside in Melbourne as I do, it is laso worth looking at other data laws throughout the world. The GDPR, introduced in 2018 is Europe's law on data use and collection and one of the harshest in the world. While more and mroe individuals and services are relying on data warehouses and cloud storage to store their data these guys have come in heavy introducing laws to curtail the over/misuse of data. The principles defined within are similar to those in Melbourne, with transparency being key as well as purpose limitation (only using collected data for the reasons specified to the data subject) and data minimization.
In this instance we could compy with these rules by, obviously, being transparent with our clientele, honest with our usage of data but also keeping data we collect to the miinimum requred to perform the tasks we need to.
Laws pertaining to storage limitations and accuracy are also very similar to those in Melbourne. Data must be kept up to date and only retained as long as it serves its intended purpose. 
Probably the most pertinent part of the GDPR however, is accountability. The act states that We will be accountable for being able to demonstrate our compliance, and to that effect should have trained staff in place to make sure we are in line with these rules at all time. This could of course jsut be as simple as staff training for a small team of one or two, however as the project (and thus the team) grow it may be pertinent to employ a full time Data orginization officer. Keeping detailed records of the storage and use of user data would also be a great way to comply. In the same way a tattoo artists keeps sterilisation records for hteir equiptment, so to should tech companies keep records of what is still often a barely understood, sometimes under-regulated but potentially very dangerous area of what they do.



### Q9 	Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.
In a relational database model data is stored in a collection of tables, each having a unique name. Within each table there are columns, which store categorical data, and rows (or tuples) that store relational data. 
For example in a database of books, a row will provide information about each element. Lets say in this example that is each book. A row may consist of a ID number, title, author, date of publication, genre, length.
The columns however will be the categorical data, so in this case there will be a column for each of the above pieces of infoprmation related to each individual book.
Each table will have a **primary key**, which is a *unique* identifier for each element. If the table is linked to another table, lets say in this case there is a table for each author's information(Auth-ID, name, nationality, age, country of residence) then a **foreign key** would be used to link the tables. In this case perhaps instead of having an author name in the original table, it wouldf have an author ID thus linking to the authors details.
Relations are represented in three basic way:
- **One to one** relations are when there is only one record on each side fo the relationship. In the above example think Author ID <-> Author name.
- **One to many** relations consist of a lopsided amount of records, with one on one side and more than one on the other. Tink for example Author ->Book1, Book2, Book3
- **Many to many** relationships are when there are multiple records on both sides of the relationship. For for academic books that have multiple authors, you would have Auth1, Auth2, Auth3 <-> Book1, Book2, Book3.

### Q10 Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.
Relational databases require integrity, otherwise data may be lost, overwritten, or become otherwise corrupted. There are three main types of integrity.
**Entity integrity** requires every entity to have a unique and not-null primary key. You will often see this as some form of ID, like UserID, where any other property of an entity could be duplicated.
**Referential integrity** requires that every foreign key *is* a primary key of another table, and that it is not of a conflicting data type. This ensures that the reference is valid and data can be retrieved.
**Domain integrity** means that every record in a domain meets the requirements specified by that domain. For example if the domain required your bank account number and you instead wrote 'bananas' this would mess up the integrity of the database.
Looking at the simple ERD below you can see that the Primary Key of Author is a NOT NULL id number instead of an author's name. This is because two or more authors could share the same name, invalidating the integrity of the entity.
You can also see that the *foreign key* in the second table is linked to the *primary key* of the first. This ensures referential integrity as the FK is directly linked to the unique PK of the first table.
<img src=./docs/bookerd.png>


### Q11 Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.
Following the CRUD methodology, the following commands are used to manipulate data in a relational database model:
**INSERT** is how we add data to a database. When inserted,  a table must be specified, data must have a primary key assigned (this can be automated) and the colums to be populated must be specified as well as what they are to be populated with. Data entered must conform to column requirements re: data type.
**DELETE** allows for the deletion of one or more (using the WHERE command) rows from a table. Tablename must be specified and care must be taken as this action is irreversible.
**UPDATE** allows for the manipulation of data contained within columns. The use of the WHERE command is essential here or else you could end up updating entire columns of information. First the table must be specified, then the new contents, then the WHERE. as with deletion, this action is irreversible. 
**SELECT** is the command used to retrieve one or many records from a table. A table must be specified (FROM) as well as at least one column that you want to see the information from. An asterisk can be used as a catch-all.
It is also imperative to make sure are **cleansing** and **preparing** appropriately. Disposing of redundant records and fixing errors in data entry will enswure an efficient running of a database.
Using the previous example of an Author-Book database, you could *insert* the authors name, which would need to be a string of x amount of characters (char(x)) NOT NULL, thus ensuring the id referenced an actual author. If an author was no longer stocked in your library, you could delete that author from your library, which would remove the redundant data so that something like a search algorithm would have an easier time finding what you were looking for. If an author changed his name, or perhaps became known by another nickname (Christopher Brookmyre is now referred to as 'Chris' Brookmyre) then the records could be updated to reflect this. This would be considered cleansing as it would ensure that there were not books related to two different authors that were in fact the same person.
To view the books of an authour tou could use the SELECT command. For example saying SELECT * FROM books WHERE author_id = {AuthorName} would give you a list of all books by that specific author. Again this is where cleansing is important. Think back in the days when you had an iPod and you would have 5 different spellings/capitalizations of the same artist's name due to dodgy downloads, and how frustrating that was. Same principle applies here but the frustration is on a much grander scale.

### Q12 Conduct research into a web application (app) and answer the following parts:   50-100 per part
I will be focusing on **Uber** for this question
- a. List and describe the software used by the app.
For application and data:
Python, Java, Swift, Golang, Objective-C, Java - Programming Language
JQuery, Backbone.js, React - Javascript Library
Node.js - Application building
NGINX - API
MySQL, PostgreSQL, MongoDB, Redis, Cassandra(NoSQL), Riak (NoSQL)- Database
Amazon EC2 - Cloud
Kafka - Realtime Data feeds
Apache Thrift - Cross language services developement
RIBs - Cross platform apps (iOS/Android)
AresDB - Analytics
Hadoop, Apache Spark - Data storage and processing

Utilities:
Google Analytics, Mixpanel, Heap - Analytics
Elasticsearch - RESTful search engine
PayPal, Braintree - Payment
Twilio - Voice & messaging
Twilio SendGrid - Email
TensorFlow - Library for Machine intelligence
HackerOne - Security
Ludwig - Deep learning

DevOps:
Sentry - Mainenance/performance
RequireJS - JS file/module loader
Prometheus - monitering/alerts
Puppet Labs - configuration management
Nagios - systems/network/infrastructure monitering 
Zookeeper, M3, - distribution of cloud
Graphite - graphing (performance)
Jaeger - tracing transactions between services
Brunch - HTML 5 Building
uberalls - Location intelligence (communication between different locations)
Zap - Security
Kraken by Uber - P2P networking
Peloton - Resource scheduling

Business Tools:
Zendesk - Customer service
Mattermost - Chat (uChat)
Delighted - Customer Feedback

- b. Describe the hardware used to host the app.
While technically using a hybrid model of cloud (Amazon EC2, Amazon S3) and data centers, Uber relies heavily on Amazon Web services to facilitate their app. Event he clouds fall back to Ammazon servers. They have a ratio of two clouds to one on-site server and hardware in the field relays to the nearest server, wherever that may be. If the nearest server fails, then it will bounce across to the next nearest one and so on.
Hadoop is also used which involves a 'data warehouseing' situation to store large amounts of unstructured data.
- c. Describe the interaction of technologies within the app
The interaction of technologies within this app are vast and complex, with HackerOne and Sentry finding vulnerabilites and bugs before anyone nefarious does, as well as Zap providing authentication software. Mattermost and Twilio (+SendGrid) handle in app communications while Paypal handling payments and Braintree backing them up with things like money conversion.
Uber have gradually been writing their own software to integrate into their systems, some piggybacking on existing software and others just a purpose built piece of software, but understanding the global implications of even the smallest change these developments must be craefully orchestrated, not jsut for profits but for customer and cotractor safety.
- d. Describe the way data is structured within the app
Data within the app is structured in both relational databases and unstructured data depending. Meta data is collected in an unstructured way in massive amounts whereas for both security and efficiency reasons user/contractor data is stored using the RDBM.
- e. Identify entities which must be tracked by the app
Customer - Name, past trips, payment info, phone, address, email, password
Driver - Name, car info, payment info, phone, address, email, password
Car - Rego, age, make & model, Roadworthy date, colour
Trip - Time, destination, source, meta details
Payment - Credit Card, Exp Date, CCV
- f. Identify the relationships and associations between the entities you have identified in part (e)
Trip has one customer
Customer has many trips
Trip has one driver
Driver has many trips
Trip has one fare
Fare has one trip
Trip has one payment
Payment has one trip
Trip has one car
Car has many trips
Trip has many locations
Location has many trips
Trip has many ratings
Ratings have many trips
Ratings are for many trips
Ratings are for many customers
Ratings are for many drivers
Drivers have many ratings
Customers have many ratings
Locations have one map ID
Map IDs have one location
Locations have one address
Addresses have one location
Customers have many payid
Payid has one customer
Driver has one car
Car has one driver

- g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)
<img src=./docs/ubererd.png>



### References:
While I have not directly used any info from websites, along with EdStem and the lessons provided by my educators I found these sites very helpful:
**Agile**:
https://agilemanifesto.org/
https://hive.com/blog/what-is-agile-project-management-methodology/
**Manual Testing**
https://www.browserstack.com/guide/manual-testing-tutorial Jash Unadkat, Technical Content Writer at BrowserStack - December 11, 2021
**Privacy Policy**
https://ovic.vic.gov.au/privacy/information-privacy-principles-full-text/
https://content.legislation.vic.gov.au/sites/default/files/2022-08/14-60aa028%20authorised.pdf
https://gdpr.eu/what-is-gdpr/
**Security**
https://www.dnv.com/article/the-three-pillar-approach-to-cyber-security-data-and-information-protection-165683
**PostgreSQL**
https://www.cybertec-postgresql.com/en/postgresql-overview/advantages-of-postgresql/
https://www.guru99.com/introduction-postgresql.html
https://www.oreilly.com/library/view/sql-and-relational/9781449319724/ch01s04.html
**App Architecture**
https://www.simform.com/blog/web-application-architecture/
**Stack information**
https://stackshare.io/uber-technologies/uber#stack
https://theappsolutions.com/blog/development/uber-tech-stack/
**Uber Info**
https://uber.com