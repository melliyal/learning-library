# Introduction

This section of the workshop highlights enhancements in Oracle Database 21c to improve the security of passwords.

Estimated Time: 60 minutes

## Administration in Oracle Database 21c

Starting in this release, the parameter to enable or disable password file case sensitivity is removed. All passwords in new password files are case-sensitive.

Case-sensitive password files provide more security than older password files that are case insensitive. Oracle recommends that you use case-sensitive password files. However, upgraded password files from earlier Oracle Database releases can retain their original case-insensitivity. You can force your password files to be case-sensitive by migrating password files from one format to another.

### Labs

* Upgraded Password File Case Sensitivity
* Password Length Enforcement

### Prerequisites

* An Oracle Cloud Account - Please view this workshop's landing page to see which environments are supported
* Working knowledge of vi

> **Note:** If you have a **Free Trial** account, when your Free Trial expires your account will be converted to an **Always Free** account. You will not be able to conduct Free Tier workshops unless the Always Free environment is available. **[Click here for the Free Tier FAQ page.](https://www.oracle.com/cloud/free/faq.html)***

## About Oracle Database 21c

The 21c generation of Oracle's converged database offers customers; best of breed support for all data types (e.g. relational, JSON, XML, spatial, graph, OLAP, etc.), and industry leading performance, scalability, availability and security for all their operational, analytical and other mixed workloads.

 ![Oracle DB 21c Advantages](images/21c-support.png "Oracle DB 21c Advantages")
Key updates made in Database 21c are:
* JSON binary data type
* Blockchain tables
* Auto machine learning with Python
* Enhancements for sharding, database in-memory and graph analytics.

With 21c, customers can
* Reduce IT cost and complexity
* Unlock innovation
* Develop powerful, data-driven applications

## Learn More

* [Oracle Database Blog](http://blogs.oracle.com/database)
* [Introducing Oracle Database 21c](https://blogs.oracle.com/database/introducing-oracle-database-21c)

## Acknowledgements

* **Author** - Donna Keesling, Database UA Team
* **Contributors** - Kay Malcolm, David Start, Kamryn Vinson, Anoosha Pilli, Tom McGinn, Database Product Management
* **Last Updated By/Date** - Kay Malcolm, November 2020
