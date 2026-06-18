🌐 Website Health Monitoring & Email Alert System
<p align="center"> <img src="https://img.shields.io/badge/n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" /> <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /> <img src="https://img.shields.io/badge/Automation-Active-brightgreen?style=for-the-badge" /> </p>
📌 Overview

An automated website monitoring workflow built with n8n that continuously checks website availability and instantly sends email notifications based on HTTP response status codes.

This workflow can be used for:

E-commerce websites
Portfolio websites
SaaS applications
Business websites
Landing pages

The system automatically detects downtime and server issues, ensuring website owners are notified immediately.

✨ Features
⏰ Scheduled website monitoring
🌐 HTTP status code tracking
🔀 Intelligent routing using Switch Node
📧 Automated Gmail alerts
🚨 Downtime notifications
🛡️ Fallback error handling
⚡ Real-time monitoring
📝 Customizable email templates
🏗 Workflow Architecture
Schedule Trigger
        │
        ▼
HTTP Request
        │
        ▼
Switch (Status Code Check)
        │
 ┌──────┼──────┬──────┬──────┬──────┐
 ▼      ▼      ▼      ▼      ▼      ▼

200    404    500    502    503   Other
 │      │      │      │      │      │
 ▼      ▼      ▼      ▼      ▼      ▼

Edit Fields → Gmail Alert
📊 Status Handling
Status Code	Description	Action
200	Website Online	Success Email
404	Not Found	Warning Email
500	Internal Server Error	Critical Alert
502	Bad Gateway	Critical Alert
503	Service Unavailable	Critical Alert
Other	Unexpected Response	Fallback Alert
🛠 Technologies Used
n8n
Gmail
HTTP Request Node
Switch Node
Edit Fields Node
Schedule Trigger
⚙️ Setup
1. Import Workflow

Import the provided workflow JSON into your n8n instance.

2. Configure Gmail

Add Gmail credentials using:

OAuth2
or
App Password
3. Update Website URL

Replace the URL in the HTTP Request node with the website you want to monitor.

Example:

https://yourwebsite.com
4. Activate Workflow

Enable the workflow and monitoring will begin automatically.

📧 Example Alert
Website Online
Subject: ✅ Website is Online

The monitored website is responding normally.

Status Code: 200
Server Error
Subject: 🚨 Website Server Error

The monitored website returned:

Status Code: 500

Immediate attention may be required.
📸 Workflow Screenshot

Add your workflow screenshot here.

assets/workflow.png
🚀 Use Cases
E-commerce store monitoring
Portfolio website monitoring
SaaS uptime monitoring
Landing page health checks
Client website monitoring
📄 License

MIT License

⭐ If you found this project useful, consider giving it a star.
