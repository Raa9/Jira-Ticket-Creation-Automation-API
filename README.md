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
- github account

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

- JIRA_URL=<your-jira-instance-url>
- JIRA_USERNAME=<your-jira-username>
- JIRA_API_TOKEN=<your-jira-api-token>
- PROJECT_KEY=<your-jira-project-key>
- ISSUE_TYPE=<default-issue-type>

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

save and exit the vi
```bash
:wq!
```

## Running the Application

To run the Flask application, use the following command:
```bash
python3 createjira.py
```
This will start the Flask server on http://0.0.0.0:5000/.

## Usage

### Webhook Setup

- Set up a webhook in your issue tracking system to send a POST request to the Flask API when a comment is made. The webhook should trigger when the comment body starts with /jira.

### Triggering JIRA Ticket Creation
When a comment starts with /jira, the Flask API will create a JIRA ticket using the information provided.


This README should cover all the essential details to get your project up and running, as well as provide instructions for configuring and using it.



