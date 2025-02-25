# Create APM Domain and obtain Data Upload Endpoint and Data Keys

## Introduction

In this lab, you will use the Oracle Cloud console to create an APM Domain. You will acquire Data Upload Endpoint and Data Keys, that you will use to configure APM Java Agent on the application.

Estimated time: 10 minutes

### Objectives

*	Create an APM Domain
*	Obtain a Data Upload Endpoint, a Private Data Key, and a Public Data Key


### Prerequisites

* This lab requires an [Oracle Cloud account](https://www.oracle.com/cloud/free/). You may use your own cloud account, or a Free Tier account, a cloud account that you obtained through a trial.
* To create APM domain, you will need an Oracle Cloud Account Administrator role or manage apm-domains permission in the target compartment. For more details, refer to the OCI Documentation, [Create an APM Domain](https://docs.oracle.com/en-us/iaas/application-performance-monitoring/doc/create-apm-domain.html).

## Task 1: Create an APM domain

1.	From the OCI menu, select **Observability & Management**, then **Administration**.
	![Oracle Cloud console Menu](images/2-1-domain.png " ")
2.	Click **Create APM Domain**.
  ![Oracle Cloud console, Create APM Domain](images/2-2-domain.png " ")
3. Name your APM domain and select the compartment you created during the with **[Migrating WebLogic Server to Kubernetes on OCI](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850)** workshop.

4. Add a check to the **Create as Always Free Domain**, then click **Create**.
  ![Oracle Cloud console, Create APM Domain](images/2-3-domain.png " ")

5.	This may take few minutes. Press the refresh button periodically to check the status.
  ![Oracle Cloud console, Create APM Domain](images/2-4-domain.png " ")
6.	Once the job is completed, the status turns to Active with a green icon.
  ![Oracle Cloud console, Create APM Domain](images/2-5-domain.png " ")
  For more details how to create an APM Domain, refer to the OCI documentation, [Create an APM Domain](https://docs.oracle.com/en-us/iaas/application-performance-monitoring/doc/create-apm-domain.html).

## Task 2: Obtain Data Upload Endpoint and Data Keys

To upload observations to an APM domain, Data Upload Endpoint and Data Keys must be configured in the application’s configuration files. Next you are going to obtain the values for them and then enter them into the Oracle Cloud console.

1.	Click the link to the APM domain just created.
  ![Oracle Cloud console, APM Domain](images/3-1-domain.png " ")

2. From the APM Domain Details page, in the **APM Domain Information**  section, locate the **Data Upload Endpoint**, then click **Copy**. Also paste the copied value to a text file and save as you will need this endpoint later in the workshop.  

3. In the **Data Keys**, section you find the **auto\_generated\_private_data\_key**. Click **Copy** and save the private key value to a text file.


  ![Oracle Cloud console, APM Domain](images/3-2-domain.png " ")

> ***NOTE*** : Public datakey is used when configuring the APM Browser Agent, which is not used in this workshop.

For more details on Data Upload Endpoint and Data keys, refer to the OCI documentation, [Obtaining Data Upload Endpoint and Data keys](https://docs.oracle.com/en-us/iaas/application-performance-monitoring/doc/obtain-data-upload-endpoint-and-data-keys.html).


You may now [proceed to the next lab](#next).

## Acknowledgements

* **Author** - Yutaka Takatsu, Product Manager, Enterprise and Cloud Manageability
- **Contributors** - Steven Lemme, Senior Principal Product Manager,<br>
David Le Roy, Director, Product Management,<br>
Mahesh Sharma, Consulting Member of Technical Staff,<br>
Avi Huber, Senior Director, Product Management
* **Last Updated By/Date** - Yutaka Takatsu, January 2022
