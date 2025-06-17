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

#### 2. Bash Unencrypted Volumes

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

#### 1. cost_saving_unused_eips_and_volumes

        2.1 Purpose: Identifies unused Elastic IPs and unattached EBS volumes in AWS, aiding in cost reduction.

        2.2 Features: Checks for unused Elastic IPs, unattached EBS volumes, and generates a formatted report for review.

        2.3 Prerequisites: Requires AWS credentials and the `boto3` library installed.

        2.4 Usage: Clone the repository, run the script to check for unused resources, and output the report to the console and a text file.

        2.5 Conclusion: Helps optimize AWS costs by identifying resources that can be released or deleted.


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
