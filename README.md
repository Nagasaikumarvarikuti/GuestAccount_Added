# GuestAccount_Added

# Azure Logic App: Test-Guest_account_added  

This repository contains the Azure Logic App Test-Guest_account_added. This Logic App is designed to automatically analyze IP addresses and incidents from Microsoft Sentinel, validate reputation using VirusTotal, and log the results as comments on incidents.

## 🎯 **Purpose**  
- 🚀 Triggered by an incident in Microsoft Sentinel.  
- 🌐 Retrieves related IP addresses from the incident.  
- 🏠 Checks if the IP is private or public.  
- 🔍 If public, performs a VirusTotal lookup to check reputation.  
- 🛡️ Categorizes IP addresses as **Malicious** or **Clean** based on the reputation.  
- 📝 Logs the results in Microsoft Sentinel as a comment.  

---

## 🔄 **Workflow Overview**  
1. **⚡ Trigger** – Triggered by an incident created in Microsoft Sentinel.  
2. **📡 Get IPs** – Retrieves IP addresses from the incident.  
3. **🔎 Check IP Type** – Identifies whether the IP is private or public.  
4. **🛡️ Reputation Check** – Uses VirusTotal to check the reputation of public IPs.  
5. **📝 Log Result** – Logs the result in the incident as a comment.  
6. **📧 Email Notification** – Sends an email notification if a malicious IP is detected.  

---

## 🔌 **Connectors Used**  
- 🛡️ **Microsoft Sentinel** – To retrieve and update incidents.  
- 🦠 **VirusTotal** – For IP reputation checks.  
- 📊 **Azure Monitor** – For log analysis.  
- 📧 **Office365** – For sending email notifications.

✅ Best Practices
🔑 Ensure that the VirusTotal API key is secure.
📊 Monitor the app for failures using Azure Monitor.
🔒 Use Managed Identity instead of hardcoded credentials for better security.
🛡️ Ensure permissions for Microsoft Sentinel and VirusTotal are correctly assigned.

---

✅ Feel free to open an issue or submit a pull request if you encounter any problems! 😎

