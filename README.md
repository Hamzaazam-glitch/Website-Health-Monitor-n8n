# 🌐 Website Health Monitoring & Email Alert System

<p align="center">
  <img src="https://img.shields.io/badge/n8n-Automation-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/Gmail-Alerts-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" />
</p>

---

## 📌 Overview

An automated **website monitoring & alert system** built with **n8n** and **Gmail automation** that continuously checks website availability and instantly sends email notifications based on HTTP response status codes.

This workflow can be used for:

- E-commerce websites  
- Portfolio websites  
- SaaS applications  
- Business websites  
- Landing pages  

The system automatically detects downtime, server errors, and unexpected responses, ensuring instant alerts for quick action.

---

## ✨ Features

- ⏰ Scheduled website monitoring  
- 🌐 HTTP status code tracking  
- 🔀 Smart routing using Switch Node  
- 📧 Automated Gmail alerts  
- 🚨 Downtime notifications  
- 🛡️ Fallback error handling  
- ⚡ Real-time monitoring  
- 📝 Customizable email templates  

---

## 🏗 Workflow Architecture

```text
Schedule Trigger
        │
        ▼
HTTP Request
        │
        ▼
Switch (Status Code Check)
        │
 ┌──────┼────────┬────────┬────────┬────────┐
 ▼      ▼        ▼        ▼        ▼        ▼
200     404      500      502      503     Other
 │       │        │        │        │        │
 ▼       ▼        ▼        ▼        ▼        ▼
Email   Email    Email    Email    Email   Fallback
```

---

## 📊 Status Handling

| Status Code | Description | Action |
|------------|-------------|--------|
| 200 | Website Online | Success Email |
| 404 | Not Found | Warning Email |
| 500 | Internal Server Error | Critical Alert |
| 502 | Bad Gateway | Critical Alert |
| 503 | Service Unavailable | Critical Alert |
| Other | Unexpected Response | Fallback Alert |

---

## 🛠 Technologies Used

- n8n  
- Gmail API  
- HTTP Request Node  
- Switch Node  
- Edit Fields Node  
- Schedule Trigger  

---

## ⚙️ Setup Instructions

### 1. Import Workflow
Import the workflow JSON file into your **n8n instance**.

### 2. Configure Gmail
Set up Gmail credentials using:

- OAuth2 OR  
- App Password  

### 3. Update Website URL
Replace the URL inside HTTP Request node:

```text
https://yourwebsite.com
```

### 4. Activate Workflow
Enable the workflow in n8n to start monitoring automatically.

---

## 📧 Example Alerts

### ✅ Website Online

**Subject:** Website is Online

Website is running normally.

Status Code: 200

---

### 🚨 Server Error

**Subject:** Website Server Error

The monitored website returned:

Status Code: 500

Immediate attention is required.

---

## 📸 Workflow Screenshot

Add your workflow screenshot here:

```
assets/workflow.png
```

---

## 🚀 Use Cases

- E-commerce store monitoring  
- Portfolio website monitoring  
- SaaS uptime monitoring  
- Landing page health checks  
- Client website monitoring  

---

## 📄 License

MIT License

---

⭐ If you found this project useful, please consider giving it a star.
