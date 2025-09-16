# GAS Login System
Powerful Login &amp; Signup System with Google Sheets &amp; Apps Script

#### created by: https://gwaddons.com

#### VIDEO: https://www.youtube.com/watch?v=AELh87Qq13M

#### request source code here: https://script.google.com/macros/s/AKfycbzjQ9sre41Xh1k_nc57ijk_cV0XkilH1SzDeKMRRONuiqeU7p6iACYC6BRP65zarkPkKA/exec

[![ORIGINAL SOURCE CODE FROM GWADDONS ](https://img.shields.io/badge/Please_Use-Original_Repo-blue?style=for-the-badge&logo=github)]([https://github.com/author/original-repo](https://script.google.com/macros/s/AKfycbzjQ9sre41Xh1k_nc57ijk_cV0XkilH1SzDeKMRRONuiqeU7p6iACYC6BRP65zarkPkKA/exec))

> ⚠️ **Disclaimer:**  
> This repository is a COPY of [GWADDONS]([https://github.com/author/original-repo](https://script.google.com/macros/s/AKfycbzjQ9sre41Xh1k_nc57ijk_cV0XkilH1SzDeKMRRONuiqeU7p6iACYC6BRP65zarkPkKA/exec)).
> I have created this repo for my own purposes (e.g., testing, learning, or small modifications).
> All credit and copyright belong to the original author(s).  
> If you plan to use or contribute, please **ask for the original source code** instead of fork this repo.
>
> # Google Apps Script Setup Guide

## Table of Contents
- [Enabling Google Services/APIs (if required)](#enabling-google-servicesapis-if-required)
- [Deploying the Script as a Web App (if applicable)](#deploying-the-script-as-a-web-app-if-applicable)
- [Setting Up Triggers (if applicable)](#setting-up-triggers-if-applicable)
- [Troubleshooting Tips](#troubleshooting-tips)
- [How to Debug: Using Execution Logs](#how-to-debug-using-execution-logs)

---

## Enabling Google Services/APIs (if required)

Some scripts require access to advanced Google services (like Gmail API, Calendar API, Drive API).

1. **In the Apps Script Editor:** On the left sidebar, click **Services** (the `+` icon).  
2. **Find and Add:** Browse the list of services. If the script’s instructions mention a specific API (e.g., *"Please enable the Drive API"*), find it, click **Add**, and confirm in the pop-up.  
3. **Authorization:** The first time your script runs and tries to use an enabled service, Google will ask you to authorize it. Follow the on-screen prompts.  

---

## Deploying the Script as a Web App (if applicable)

If your automation includes a user interface (like a form or dashboard) accessible via a web link, you need to deploy it as a Web App.

1. **In the Apps Script Editor:** Go to **Deploy > New deployment**.  
2. **Select Deployment Type:** Choose **Web app**.  
3. **Configuration:**
   - **Execute as:** Set this to *Me* (your email address).  
   - **Who has access:** Choose *Anyone* (or more restrictive options if for internal use).  
   - **Description:** (Optional) Add a short description for this deployment.  
4. **Deploy:** Click **Deploy**.  
5. **Authorization:** On first deploy, you’ll be prompted to review permissions. Select your Google account and click **Allow**.  
6. **Get Web App URL:** After deployment, copy the generated URL — this is your app’s public link.  
7. **Update Deployment for Changes:** For any code updates, go to **Deploy > Manage deployments**, edit, and create a new version.  

---

## Setting Up Triggers (if applicable)

Triggers let scripts run automatically based on events or schedules.

1. **In the Apps Script Editor:** Click **Triggers** (clock icon).  
2. **Add Trigger:** Click the **+ Add Trigger** button.  
3. **Configure Your Trigger:**
   - **Choose function to run:** Select the target function (e.g., `onFormSubmit`, `processEmails`, `runDailyReport`).  
   - **Choose deployment:** Select your Web App project.  
   - **Select event source:**
     - *From spreadsheet*: `onEdit`, `onChange`, `onFormSubmit`  
     - *Time-driven*: run daily, hourly, etc.  
     - *From form*: for direct Google Form connections  
     - *From calendar*: for Calendar-based scripts  
   - **Select event type:** (e.g., *On open*, *On edit*, *On form submit*, *Day timer*, *Hour timer*).  
   - **Failure notifications:** Set frequency for error alerts.  
4. **Save** and authorize if prompted.  

---

## Troubleshooting Tips

### Permissions/Authorization Errors
- **Issue:** Script fails with *"Authorization required"*.  
- **Solution:** Run a function directly from the editor (click **Run**) to retrigger the authorization prompt.  

### Web App Not Working / Changes Not Appearing
- **Issue:** Web app doesn’t load or reflect changes.  
- **Solution:**  
  - Create a new deployment version.  
  - Clear your browser cache or use Incognito mode.  

### Script Not Running Automatically (Triggers)
- **Issue:** Trigger doesn’t fire.  
- **Solution:**  
  - Check **Triggers** setup in the editor.  
  - Use **Executions** log to view run attempts and errors.  

### "Sheet/Doc/Folder not found" Errors
- **Issue:** Script can’t locate required files.  
- **Solution:** Verify IDs (Spreadsheet ID, Document ID, Folder ID) and sharing permissions.  

### API Not Enabled Errors
- **Issue:** Errors mentioning GmailApp, DriveApp, etc.  
- **Solution:** Ensure required services are enabled in **Services**.  

### Script Exceeding Execution Limits
- **Issue:** Script times out or exceeds memory.  
- **Solution:** Optimize code or break tasks into smaller chunks.  

---

## How to Debug: Using Execution Logs

The **Executions** log in Apps Script Editor shows:
- Every run attempt (manual or trigger-based).  
- Status (success, failed, timed out).  
- Exact error message and line number on failure.  

This is your most valuable debugging tool.




