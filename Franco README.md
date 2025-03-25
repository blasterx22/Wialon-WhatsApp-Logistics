# Wialon – WhatsApp – Logistics Integration

**Automated Order Creation in Logistics Triggered by Wialon Notification and WhatsApp Confirmation**

This workflow automates the process of creating delivery orders in the Wialon Logistics module. When a low tank level is detected by Wialon, a WhatsApp message is automatically sent to the responsible person requesting refill approval. Upon confirmation, an order is scheduled in Logistics within the appropriate time window.

The system uses **n8n** as the automation engine, **Supabase** for data storage and tracking, and the **WhatsApp Cloud API** for client interaction. The entire process is fully automated, from alert to order creation.

---

## 🔧 Technologies Used

- **n8n** – Open-source automation engine  
- **Wialon** – GPS tracking and tank monitoring  
- **Logistics app (Wialon)** – Order and delivery management  
- **Supabase (PostgreSQL)** – Backend for storing request and response data  
- **WhatsApp Business Cloud API** – Client messaging and interactive approvals  

---

## 🔁 Workflow Overview

1. Wialon detects a low tank level and triggers a webhook.
2. n8n processes the data and stores it in Supabase.
3. A WhatsApp message with **Approve** / **Decline** buttons is sent.
4. Upon **approval**, an order is created in Logistics with calculated delivery timing.
5. The system confirms the operation via WhatsApp and updates the status in Supabase.

---

## 🧠 Smart Features

- 📅 Dynamic scheduling based on approval time (with cutoff logic).
- ✅ Prevents duplicate responses by checking existing status.
- ⏱️ Calculates response time and flags delays.
- 🗃️ Persists full request and response history in Supabase.
- 🔄 Feedback loop with automatic status updates to the user.

---

## 📁 Repository Contents

- `Wialon___Logistics.json` – Exported n8n workflow
- `README.md` – Full project documentation

---

## 📌 Example Use Case

> "The tank at Site A is below 20%."  
→ WhatsApp alert to operator  
→ Operator taps "Approve"  
→ Order is automatically created in Wialon Logistics  
→ Operator receives confirmation with estimated service time

---

## 🚀 Future Improvements

- 🧾 Let users retrieve recent orders by sending a WhatsApp keyword (e.g. `"My orders"`)
- 📊 Dashboard with response metrics and refill history

---

## 🧱 Built by

Franco Cortez – Project Implementation Manager  
March 2025  
