# GuestAccount_Added

This repository contains the Azure Logic App Test-Guest_account_added. ThisLogic App is designed to automate the analysis of incidents generated in Microsoft Sentinel. It retrieves related IP addresses from the incident, checks their reputation using VirusTotal, and determines if they are malicious or clean. Additionally, it verifies if the user is the owner of the group using Microsoft Graph API and logs the results as comments in the incident. If any suspicious activity is detected, it sends an email notification to the SOC team for further action.

## 🎯 **Purpose**  
- 🚀 Triggered by an incident in Microsoft Sentinel.  
- 🌐 Retrieves related IP addresses from the incident.  
- 🏠 Checks if the IP is private or public.  
- 🔍 If public, performs a VirusTotal lookup to check reputation.  
- 🛡️ Categorizes IP addresses as **Malicious** or **Clean** based on the reputation.  
- 📝 Logs the results in Microsoft Sentinel as a comment.  
- 🔑 **Validates if the user is the owner of the group** using Microsoft Graph API.  

---

## 🔄 **Workflow Overview**  
1. **⚡ Trigger** – Triggered by an incident created in Microsoft Sentinel.  
2. **📡 Get IPs** – Retrieves IP addresses from the incident.  
3. **🔎 Check IP Type** – Identifies whether the IP is private or public.  
4. **🛡️ Reputation Check** – Uses VirusTotal to check the reputation of public IPs.  
5. **👤 Group Ownership Check** – Uses Graph API to verify if the user is the owner of the group.  
6. **📝 Log Result** – Logs the result in the incident as a comment.  
7. **📧 Email Notification** – Sends an email notification if a malicious IP is detected.  

---

## 🔌 **Connectors Used**  
- 🛡️ **Microsoft Sentinel** – To retrieve and update incidents.  
- 🦠 **VirusTotal** – For IP reputation checks.  
- 🔍 **Microsoft Graph API** – To check if the user is the owner of the group.  
- 📊 **Azure Monitor** – For log analysis.  
- 📧 **Office365** – For sending email notifications.  

---

## ✅ **Best Practices**  
- 🔑 Ensure that the VirusTotal API key is secure.  
- 📊 Monitor the app for failures using Azure Monitor.  
- 🔒 Use Managed Identity instead of hardcoded credentials for better security.  
- 🛡️ Ensure permissions for Microsoft Sentinel and VirusTotal are correctly assigned.  

---

✅ **Feel free to open an issue or submit a pull request if you encounter any problems!** 😎  
