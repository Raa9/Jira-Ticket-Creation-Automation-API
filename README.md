# JIRA TICKET CREATION AUTOMATION API

## Overview

This project automates the creation of JIRA tickets using a webhook. The system listens for specific comments on issues, and when a comment starts with `/jira`, it triggers a webhook that interacts with a Python Flask API to create a JIRA ticket.

**Key Features:**
- Webhook integration with JIRA to automate ticket creation.
- Python API built with Flask running on an EC2 instance.
- JIRA ticket creation triggered by specific comment patterns.

## Installation

### Prerequisites

- Python 3.x
- Flask
- An EC2 instance (or any server where you can run Python applications)
- JIRA account with API access

### Clone the Repository

```bash
git clone https://github.com/Raa9/Jira-Ticket-Creation-Automation-API.git
cd Jira-Ticket-Creation-Automation-API
```

### Install the Dependencies

Install the required Python packages using `pip`:

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

go to .env file in the project directory and add your JIRA credentials and other configurations:

```bash
#listing the .env file
ls -a
```

edit the .env file
```bash
vi .env
```

add your credential 

- JIRA_URL=<your-jira-instance-url>
- JIRA_USERNAME=<your-jira-username>
- JIRA_API_TOKEN=<your-jira-api-token>
- PROJECT_KEY=<your-jira-project-key>
- ISSUE_TYPE=<default-issue-type>





