# Create SSH Keys

## Introduction

The SSH (Secure Shell) protocol is a method for secure remote login from one computer to another. SSH enables secure system administration and file transfers over insecure networks using encryption to secure the connections between endpoints. SSH keys are an important part of securely accessing Oracle Cloud Infrastructure compute instances in the cloud.

If you already have an SSH key pair, you may use that to connect to your environment. We recommend you use the *Oracle Cloud Shell* to interface with the Oracle Cloud Infrastructure compute instance you will create. Oracle Cloud Shell is browser-based, does not require installation or configuration of anything on your laptop, and works independently of your network setup. However, if you prefer to connect through your laptop, please select an option based on your configuration.

*IMPORTANT:  If the SSH key is not created correctly, you will not be able to connect to your environment and will get errors.  Please ensure you create your key properly.*

Estimated Total Lab Time: 10 minutes

### Workshop Objectives

In this lab, you will:
* Learn how to create SSH keys by using the Oracle Cloud Shell

### Prerequisites
This workshop section requires having completed the previous section and having access to an Oracle Cloud account.

## Oracle Cloud Shell

Watch the video below for an overview of the Generate SSH Keys Cloud Shell option.
[](youtube:oq2Hk1Yy9Cg)

The Cloud Shell machine is a small virtual machine running a Bash shell which you access through the Oracle Cloud Infrastructure Console (Homepage). Cloud Shell comes with a pre-authenticated Oracle Cloud Infrastructure CLI (Command Line Interface), set to the Console tenancy home page region, as well as up-to-date tools and utilities. To use the Cloud Shell machine, your tenancy administrator must grant the required IAM (Identity and Access Management) policy.


## Tasks

1.  To start the Oracle Cloud shell, go to your Cloud console and click the cloud shell icon at the top right of the page.

    ![](./images/cloudshellopen.png " ")

    ![](./images/cloudshellsetup.png " ")

    ![](./images/cloudshell.png " ")

2.  Once the cloud shell has started, enter the following command. Choose the key name you can remember. This will be the keyname you will use to connect to any compute instances you create. Press Enter twice for no passphrase.

    ````
    <copy>mkdir .ssh</copy>
    ````

    ````
    <copy>cd .ssh</copy>
    ````

    ````
    <copy>ssh-keygen -b 2048 -t rsa -f <<sshkeyname>></copy>
    ````

    *Note: The angle brackets <<>> should not appear in your code.*

    ![](./images/cloudshell-ssh-keygen.png " ")

3.  Examine the two files that you just created.

    ````
    <copy>ls</copy>
    ````

    ![](./images/examine-cloudshell-keys.png " ")

    Note in the output that there are two files, a *private key:* ```<<sshkeyname>>``` and a *public key:* ```<<sshkeyname>>.pub```. Keep the private key safe and don't share its content with anyone. The public key will be needed for various activities and can be uploaded to certain systems as well as copied and pasted to facilitate secure communications in the cloud.

4. To list the contents of the public key, use the cat command ```cat <<sshkeyname>>.pub```

    *Note: The angle brackets <<>> should not appear in your code.*

    ![](images/cat-in-cloudshell.png " ")

5.  When pasting the key into the compute instance in future labs, make sure that you remove any hard returns that may have been added when copying. *The .pub key should be one line.*

    ![](images/copy-publickey-cloudshell.png " ")

You may now [proceed to the next lab](#next) or paste it in the LiveLabs reservation page.




## Acknowledgements
* **Author** - Dan Kingsley, Enablement Specialist, OSPA
* **Contributors** - LiveLabs Team, Tom McGinn, Kamryn Vinson, Anil Nair
* **Last Updated By/Date** - Ricardo Gonzalez, Senior Principal Product Manager, Oracle Cloud Database Migration, August 2021

