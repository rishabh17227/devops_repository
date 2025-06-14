# Ansible Playbooks

A collection of Ansible playbooks for various server setups and cloud environment automation.

---

### Contents

#### 1. Ansible Windows IIS

        1.1 Purpose: Automates the setup of IIS on a Windows server in AWS, deploying a default website.

        1.2 Structure:
        - `tasks/main.yml`: Contains the playbook for IIS configuration.
        - `templates/index.html.j2`: Provides the HTML template for the website.

        1.3 Usage: 
        - Configure target server details in `hosts.ini` and execute the playbook.

---

#### 2. Ansible AWS Automation

        2.1 Purpose: Streamlines AWS environment management across 400+ accounts, including credential setup and resource mounting.

        2.2 Features:
        - Automates credential management and mounts EFS/S3 as NFS.
        - Sets up CRON jobs for centralized log management.

        2.3 Usage: Enhances provisioning and maintenance in development and production environments.

---

# Bash Scripts

A collection of Bash scripts for automating tasks related to AWS and other utilities.

---

### Contents

#### 1. Bash External Facing AWS Instances

        1.1 Purpose: Retrieves information about EC2 instances with public IPs across specified AWS accounts, logging details into a CSV file.

        1.2 Prerequisites: Requires AWS CLI and jq for JSON processing.

        1.3 Usage: Execute the script to generate an output file with instance details.

        1.4 Output: Produces a CSV file with instance IDs, security groups, CIDR blocks, and allowed ports.

---

#### 2. Bash JS Stock Web Scraper

        2.1 Purpose: Scrapes stock prices from Screener.in and saves them in an Excel file using Node.js.

        2.2 Prerequisites: Node.js and specific npm modules must be installed.

        2.3 Setup: Predefined stock URLs and mappings for Excel output.

        2.4 Usage: Run the script with Node.js to execute the scraping process.

        2.5 Customization: Easily add stocks by updating URLs and cell mappings.

--- 

#### 3. Bash R53 Records Deletion

        3.1 Purpose: Manages DNS records in an AWS Route53 hosted zone by identifying, updating, and deleting A and TXT records.

        3.2 Prerequisites: Requires AWS CLI, jq, and access to Route53.

        3.3 Setup: Update the `HOSTED_ZONE_ID` and ensure scripts are executable.

        3.4 Usage: Run scripts to list and delete specified DNS records.

        3.5 Scripts: 
        - `script1.sh`: Lists DNS records targeted for deletion.
        - `script2.sh`: Executes updates and deletions of the listed records.

---

#### 4. Bash Trust Relationship Backup and Apply

        4.1 Purpose: Manages AWS IAM roles by verifying and updating trust relationships and policies across accounts.

        4.2 Prerequisites: Requires AWS CLI, configured profiles, and necessary JSON files.

        4.3 Usage: Modify policy files and run the script to apply changes.

        4.4 Workflow: Checks and updates role policies and backups existing trust relationships.

        4.5 Customization: Adjust the IAM role name and target AWS accounts as needed.

---

#### 5. Bash Unencrypted Volumes

        5.1 Purpose: Identifies unencrypted EC2 volumes across AWS accounts and regions, reporting details in a CSV file.

        5.2 Key Features: Loops through profiles and regions to retrieve volume details.

        5.3 Usage: Configure profile and region arrays in the script before execution.

        5.4 Output: Generates a CSV file with details including account name, volume ID, instance name, and volume size.

<br><br><br><br>

# Powershell Scripts

A collection of PowerShell scripts for automating various tasks, including network performance monitoring.

---

### Contents


#### 1. network_performance_check

        1.1 Purpose: Monitors network performance metrics like received/sent bytes, packet loss, and latency.

        1.2 Features: Logs metrics to a specified file; customizable for different network interfaces and monitoring intervals.

        1.3 Requirements: PowerShell on Windows; administrative privileges may be required.

        1.4 Usage: Save the script, edit parameters for the network interface and log file, run it in PowerShell, and check the log for results.

        1.5 Conclusion: Provides an easy way to monitor network performance with customizable options.

---

#### 2. wsl_install

        2.1 Purpose: Automates the installation of the Windows Subsystem for Linux (WSL) on Windows machines.

        2.2 Prerequisites: Requires administrative rights and is compatible with Windows 10 (version 2004 and later) and Windows 11.

        2.3 Features: Enables WSL and Virtual Machine Platform features, sets WSL to version 2 by default, and reports installation time.

        2.4 Usage: Run the script in PowerShell with administrative privileges to automate the installation process.

        2.5 Conclusion: Simplifies the setup of WSL, making it easier for users to enable Linux on Windows.





<br><br><br><br>

# Python Scripts

A collection of Python scripts for various tasks, including AWS configuration and automation.

---

### Contents

#### 1. AWS_SSO_config_generator

        1.1 Purpose: Generates AWS SSO profiles for multiple AWS accounts, simplifying the configuration process.

        1.2 Prerequisites: Requires Python 3.x and the `aws-sso-util` tool installed for credential management.

        1.3 Usage: Update the script with AWS account IDs, SSO URL, region, and role name; run the script to generate formatted profile configurations for AWS.

        1.4 Customization: Easily modify SSO start URL, region, and role name parameters as needed.

        1.5 Conclusion: Streamlines the process of setting up AWS profiles, enhancing the efficiency of AWS SSO configuration.

---

#### 2. cost_saving_unused_eips_and_volumes

        2.1 Purpose: Identifies unused Elastic IPs and unattached EBS volumes in AWS, aiding in cost reduction.

        2.2 Features: Checks for unused Elastic IPs, unattached EBS volumes, and generates a formatted report for review.

        2.3 Prerequisites: Requires AWS credentials and the `boto3` library installed.

        2.4 Usage: Clone the repository, run the script to check for unused resources, and output the report to the console and a text file.

        2.5 Conclusion: Helps optimize AWS costs by identifying resources that can be released or deleted.

---

#### 3. logs_rotation_dynamic_script

        3.1 Purpose: Automates the collection, organization, and archival of Tomcat server logs based on date ranges and specified intervals.

        3.2 Features: Organizes logs weekly, creates date-based directories, compresses logs into archives, and sends Slack notifications on errors.

        3.3 Requirements: Requires Python 3.x, specific Python packages, and a Unix/Linux environment for proper execution.

        3.4 Usage: Run the script daily using Python; it performs different operations based on the day of the week.

        3.5 Note: Designed for Unix/Linux environments with assumptions about log file naming conventions and permissions.

---

#### 4. serverless-api-aws_cdk

        4.1 Purpose: Facilitates the creation and management of a serverless API using AWS CDK in Python.

        4.2 Prerequisites: Requires Python 3 and access to the `venv` package for creating a virtual environment.

        4.3 Setup: Initialize a virtual environment, activate it, and install required dependencies from `requirements.txt`.

        4.4 Useful Commands: Includes commands for listing stacks, synthesizing CloudFormation templates, deploying stacks, and viewing documentation.

        4.5 Conclusion: Streamlines the development process of serverless applications using AWS services, leveraging the power of CDK.

---

#### 5. serverless-lambda

        5.1 Purpose: Implements an AWS Lambda function for managing a product inventory in DynamoDB, supporting HTTP methods for inventory management.

        5.2 Features: Provides health checks, product retrieval, storage, and deletion through a serverless architecture with easy API Gateway integration.

        5.3 Prerequisites: Requires an AWS account, AWS CLI, and Python 3.6 or later.

        5.4 Setup: Create a DynamoDB table, clone the repository, and install required packages using pip.

        5.5 Custom Encoder: Includes a `CustomEncoder` class for serializing Decimal objects from DynamoDB into JSON format, preventing errors during serialization.

        5.6 Deployment: Instructions for zipping the project and deploying it using the AWS CLI with the necessary permissions.

        5.7 Logging: Utilizes Python’s logging library for monitoring function execution through AWS CloudWatch.

        5.8 Conclusion: Offers a robust solution for inventory management in a serverless setup, easily extendable for additional functionality.



<br><br><br><br>

# Terraform Scripts

A collection of Terraform scripts designed for provisioning and managing infrastructure resources in a cloud environment.

---

### Contents

#### 2. tf-workspaces-setup

        2.1 Purpose: Manages AWS resources using Terraform configurations, enabling efficient infrastructure management across multiple environments.

        2.2 Features: Supports the creation and management of Terraform workspaces to handle different environments (e.g., `dev`, `test`, `prod`), along with a Makefile to simplify the workflow for planning, applying, and destroying infrastructure.

        2.3 Requirements: Requires Terraform installed and AWS credentials configured in the local environment, as well as familiarity with the command line.

        2.4 Overview: Terraform workspaces allow users to manage distinct states for different environments within a single configuration. This setup facilitates the creation of new workspaces, switching between them, and applying configurations specific to each environment seamlessly, ensuring isolated and reproducible infrastructure.

        2.5 Directory Structure: Contains an `env_vars` directory for environment-specific variable files, a `Makefile` for command automation, and a `main.tf` for the Terraform configuration.

        2.6 Workspace Management: Includes commands to create new workspaces, switch between them, and use the Makefile for planning, applying, and destroying infrastructure.

        2.7 Conclusion: Provides a streamlined approach for managing AWS infrastructure using Terraform with the added convenience of workspaces and Makefile commands.


---
