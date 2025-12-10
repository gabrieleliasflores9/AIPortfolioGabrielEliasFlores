# ⚡ Intelligent CRM & Proposal Dispatcher

## 📄 Overview
A hybrid automation engine that turns a static Google Sheet into a dynamic CRM. This system monitors lead status in real-time and triggers personalized email sequences—sending pricing, portfolios, or follow-ups instantly based on specific logic gates.

## 🎯 The Problem
Sales teams face two main operational bottlenecks:
1.  **Speed to Lead:** Manually sending a proposal 2 hours after a request dramatically lowers conversion rates.
2.  **Spreadsheet Chaos:** Tracking "Who did I email?" and "Which PDF did I send?" in a static sheet leads to errors and duplicate contacts.

## 💡 The Solution
I built a conditional workflow on **Make.com** that acts as an automated sales operations manager:

1.  **Watches the Database:** Monitors a Master Google Sheet for status changes (e.g., when a lead moves to *'Qualified'* or *'Send Quote'*).
2.  **Applies Business Logic:** Verifies conditions before acting (e.g., *Is the email valid? Has the proposal already been sent?*).
3.  **Dynamic Asset Selection:** Automatically pulls the correct PDF (Proposal A vs. Proposal B) based on the client's industry.
4.  **Executes & Updates:** Sends the personalized email via Gmail and immediately **stamps the spreadsheet** with the "Last Contacted Date" to maintain data hygiene.

## 🛠️ Tech Stack
* **Make.com** (Router Logic & Error Handling)
* **Google Sheets** (Database & Trigger Source)
* **Gmail API** (High-deliverability Sending)
* **Notion** (Extra Asset Management)

## 📸 Workflow & Logic

### 1. The Logic Core (Make.com)
The workflow uses Router modules to split traffic. It differentiates between a "New Lead" needing a brochure and a "Follow-up" needing a text-only nudge.
<img width="960" height="410" alt="2025-12-06 (10)" src="https://github.com/user-attachments/assets/736c7f97-7623-42bf-b62a-6bcc7a9f51cb" />


### 2. The Result (Client Inbox)
A fully personalized email with the correct attachment, delivered seconds after the trigger.
<img width="960" height="415" alt="2025-12-07" src="https://github.com/user-attachments/assets/363be0a8-11a6-4f22-99ac-f9dd84bed19e" />
