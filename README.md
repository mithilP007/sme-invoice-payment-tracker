# 🚀 SME Invoice & Payment Tracker

> AI-powered Invoice & Payment Tracker for SMEs using IBM watsonx Orchestrate - Automated invoice processing, payment reminders, and workflow orchestration.

[![IBM watsonx Orchestrate](https://img.shields.io/badge/IBM-watsonx_Orchestrate-blue)](https://www.ibm.com/products/watsonx-orchestrate)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hackathon](https://img.shields.io/badge/Agentic_AI-Hackathon_2025-green)](https://lablab.ai/event/agentic-ai-hackathon-ibm-watsonx-orchestrate)

## 📖 Overview

Small and Medium Enterprises (SMEs) struggle with manual invoice tracking, payment follow-ups, and workflow management. This AI-powered agent built with IBM watsonx Orchestrate automates the entire invoice-to-payment lifecycle, saving time and reducing errors.

### 🎯 Problem Statement

- Manual invoice processing wastes 15-20 hours per week for SMEs
- Late payment follow-ups lead to cash flow issues
- Tracking invoices across emails, cloud storage, and spreadsheets is chaotic
- No unified system for payment status visibility

### ✨ Solution

An intelligent AI agent that:

1. **Extracts invoices** from emails and cloud storage (Gmail, Google Drive)
2. **Processes invoice data** using AI document parsing
3. **Updates tracking spreadsheet** automatically
4. **Sends payment reminders** via email and Slack/Teams
5. **Notifies teams** when payments are received or overdue
6. **Provides dashboard** for real-time payment status

---

## 🏗️ Architecture

```
┌─────────────────────┐
│   Email/Drive API   │
│  (Invoice Sources)  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────────────┐
│   IBM watsonx Orchestrate Agent     │
│                                     │
│  ┌──────────────────────────────┐  │
│  │  Document Processing Skills  │  │
│  │  - Extract Invoice Data      │  │
│  │  - Parse Vendor/Amount/Date  │  │
│  └──────────────────────────────┘  │
│                                     │
│  ┌──────────────────────────────┐  │
│  │  Workflow Orchestration      │  │
│  │  - Update Spreadsheet        │  │
│  │  - Send Reminders            │  │
│  │  - Notify Team               │  │
│  └──────────────────────────────┘  │
└─────────────────────────────────────┘
           │
           ▼
┌─────────────────────────────────────┐
│        Integrations                 │
│  • Google Sheets (Tracking)         │
│  • Gmail (Reminders)                │
│  • Slack/Teams (Notifications)      │
└─────────────────────────────────────┘
```

---

## 🎬 Demo

🔗 **Live Demo**: [Coming Soon]

📹 **Video Presentation**: [Coming Soon]

---

## 🛠️ Technologies Used

- **IBM watsonx Orchestrate**: Agent orchestration and workflow automation
- **Python**: Backend logic and API integration
- **Flask/FastAPI**: Web application framework
- **Google APIs**: Gmail, Drive, Sheets integration
- **Slack/Teams API**: Team notifications
- **Streamlit**: Dashboard UI
- **Docker**: Containerization

---

## 📦 Project Structure

```
sme-invoice-payment-tracker/
├── agent/
│   ├── watsonx_orchestrate_config.yaml
│   ├── skills/
│   │   ├── invoice_extractor.py
│   │   ├── payment_reminder.py
│   │   └── notification_sender.py
│   └── workflows/
│       └── invoice_workflow.json
├── backend/
│   ├── app.py
│   ├── api/
│   │   ├── invoice_routes.py
│   │   └── payment_routes.py
│   └── services/
│       ├── gmail_service.py
│       ├── sheets_service.py
│       └── slack_service.py
├── frontend/
│   ├── dashboard.py
│   └── static/
├── data/
│   └── sample_invoices/
├── tests/
├── docs/
│   ├── SETUP.md
│   ├── API.md
│   └── ARCHITECTURE.md
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- IBM watsonx Orchestrate account (30-day free trial)
- Google Cloud Project with Gmail, Drive, Sheets APIs enabled
- Slack/Teams webhook (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/mithilP007/sme-invoice-payment-tracker.git
   cd sme-invoice-payment-tracker
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys
   ```

4. **Configure IBM watsonx Orchestrate**
   - Follow instructions in `docs/SETUP.md`
   - Import agent configuration from `agent/watsonx_orchestrate_config.yaml`

5. **Run the application**
   ```bash
   # Backend API
   python backend/app.py
   
   # Dashboard (separate terminal)
   streamlit run frontend/dashboard.py
   ```

---

## 📊 Features

### Core Features

✅ **Automated Invoice Extraction**
- Fetches invoices from Gmail attachments and Google Drive
- AI-powered document parsing to extract vendor, amount, invoice number, due date

✅ **Smart Tracking**
- Auto-updates Google Sheets with invoice details
- Tracks status: Pending, Paid, Overdue
- Calculates days until/past due date

✅ **Payment Reminders**
- Automated email reminders 7 days before due date
- Follow-up reminders on due date and 3 days after
- Customizable reminder templates

✅ **Team Notifications**
- Slack/Teams notifications for new invoices
- Alerts for overdue payments
- Payment confirmation notifications

✅ **Dashboard**
- Real-time payment status overview
- Charts and analytics
- Export reports

### Advanced Features

🔮 **AI Insights**
- Predicts payment likelihood based on vendor history
- Identifies payment pattern anomalies

🔄 **Workflow Automation**
- Multi-step approval workflows
- Integration with accounting software (QuickBooks, Xero)

---

## 🎯 Use Cases

1. **Freelancers & Consultants**: Track client invoices and automate follow-ups
2. **Small Businesses**: Manage vendor invoices and payment schedules
3. **Startups**: Streamline accounts payable without dedicated finance team
4. **Service Companies**: Monitor recurring subscription invoices

---

## 🧪 Testing

Run tests:
```bash
pytest tests/
```

Test coverage:
```bash
pytest --cov=backend --cov=agent tests/
```

---

## 📚 Documentation

- [Setup Guide](docs/SETUP.md)
- [API Reference](docs/API.md)
- [Architecture](docs/ARCHITECTURE.md)
- [watsonx Orchestrate Configuration](docs/WATSONX_CONFIG.md)

---

## 🏆 Hackathon Submission

This project was built for the **Agentic AI Hackathon with IBM watsonx Orchestrate** (November 2025).

**Team**: Mithil P  
**Event**: [Lablab.ai Hackathon](https://lablab.ai/event/agentic-ai-hackathon-ibm-watsonx-orchestrate)

---

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Mithil P**
- GitHub: [@mithilP007](https://github.com/mithilP007)
- Email: mithil1323@gmail.com

---

## 🙏 Acknowledgments

- IBM watsonx Orchestrate team for the amazing AI agent platform
- Lablab.ai for organizing the hackathon
- Open source community for the tools and libraries

---

## 📞 Support

For questions or support:
- Open an issue on GitHub
- Contact: mithil1323@gmail.com

---

**Built with ❤️ using IBM watsonx Orchestrate**
