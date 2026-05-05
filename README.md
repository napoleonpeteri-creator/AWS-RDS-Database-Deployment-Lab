AWS-RDS-Database-Deployment-Lab
Setting up "AWS RDS" so that administrators spend less time in operational tasks, such as patching and managing database infrastructure and also improve database availability and efficiency.


Step 1 — Search for Database Services

![Step 1](images/DATABASE_SEARCH.png)

In the top navigation bar search box, type: **database insights**
From the results under Services, review available options such as RDS, DynamoDB, and Database Migration Service.



Step 2 — AMI Catalog

![Step 2](images/STEP2_AMI-CATALOGUE.png)

In the left navigation pane, click **AMI Catalog**.
This section provides available machine images used to launch instances.



Step 3 — AMI SQL Search

![Step 3](images/STEP3_AMI_CONCEPT.png)

An Amazon Machine Image (AMI) provides the software required to set up and boot an EC2 instance.

In the AMIs search box, type: **sql**
Review the available SQL-related AMIs provided by AWS, Marketplace, and the community.



Step 4 — Database Migration Service

![Step 4](images/DMS.png)

Search for **DMS** in the AWS console.
Select **Database Migration Service** to explore migration capabilities for moving databases into AWS.



 RDS Database Creation

 Configuration 1 — Enter RDS & Create Database

![Configuration 1](images/Create_DB.png)

Navigate to **Databases** in the RDS console.
Click **Create database** to begin the deployment process.



Configuration 2 — Choose Creation Method & Engine

![Configuration 2](images/database_engine.png)

For database creation method, choose **Standard create**.
Under Engine options, select **MariaDB**.



Configuration 3 — Engine Version, Template & DB Identifier

![Configuration 3](images/DB_Configuration1.png)

Keep the default **MariaDB engine version**.
For Templates, choose **Dev/Test**.

For DB instance identifier, type:
**my-database**



Configuration 4 — Credentials Settings

![Configuration 4](images/Configuration2.png)

For Master username, keep the default: **admin**

For Credentials management, choose **Self managed**

For Master password, type your password and confirm it.



Configuration 5 — Instance & Storage

![Configuration 5](images/Configuration3.png)

For DB instance class, choose **Burstable classes**

Select instance type: **db.t3.xlarge**

For Storage type, choose **General Purpose SSD (gp3)**

For Allocated storage, type: **20 GiB**



Configuration 6 — Storage Autoscaling & Multi-AZ

![Configuration 6](images/Configuration4.png)

Enable **Storage autoscaling**

For Maximum storage threshold, keep: **1000 GiB**

For Multi-AZ deployment, choose:
**Create a standby instance**



Configuration 7 — Networking & Security

![Configuration 7](images/Configuration5.png)

For Virtual Private Cloud (VPC), keep the **default VPC**

For DB subnet group, keep **default**

For Public access, select **No**

For VPC security group, choose **existing**



Configuration 8 — Monitoring Settings

![Configuration 8](images/Configuration6.png)

For Monitoring, keep **Database Insights – Standard**

Disable **Performance Insights**

Under Additional monitoring settings, disable **Enhanced Monitoring**



Configuration 9 — Database Options & Backup

![Configuration 9](images/Configuration7.png)

Expand **Additional configuration**

For Initial database name, type:
**my_database**

Review default DB parameter group and option group

Ensure **automated backups** are enabled



Configuration 10 — Encryption & Maintenance

![Configuration 10](images/Configuration8.png)

Review default **encryption settings (AES-256)**

Disable **Enable auto minor version upgrade**

For Maintenance window, keep: **No preference**

Scroll down and click **Create database**



Verification

Configuration 11 — Database Created

![Configuration 11](images/Configuration9.png)

After creation, wait a few minutes.

Confirm that the database status changes to: **Available**

---

Configuration 12 — Database Details & Actions

![Configuration 12](images/Configuration10.png)

Click on **my-database** to view details

Review endpoint, port, and connectivity settings

Under **Actions**, explore options such as creating read replicas and managing the instance
