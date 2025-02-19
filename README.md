# Sendmail Wrapper for Linux

## Overview
This project provides a native shell script wrapper for `sendmail` on Linux-based servers. The main purpose of this wrapper is to **log all outgoing emails**, store email metadata and content in a database via a webhook, and pass the original email to the actual `sendmail` binary **without modification**.

This solution ensures that all emails sent via PHP scripts, cron jobs, and system-generated messages are **logged effectively**.

## Features
- ✅ Logs all outgoing emails, including:
  - **To**, **From**, **Cc**, **Bcc**, **Subject**, **Body**, and **Attachments**
- ✅ Stores logs in a specified log file
- ✅ Sends email data to a webhook for database storage
- ✅ Passes the email unmodified to the actual `sendmail`
- ✅ Works seamlessly with PHP mail, cron jobs, and system-generated emails

---

## Installation

### 1️⃣ Backup Existing Sendmail Binary
Before replacing `sendmail`, make a backup of the existing binary:
```bash
sudo mv /usr/sbin/sendmail /usr/sbin/sendmail.real
```

### 2️⃣ Create the Sendmail Wrapper Script
Create a new file /usr/sbin/sendmail and add the wrapper script. Ensure the script logs email details and passes the original email to the actual sendmail.
### 3️⃣ Set Executable Permissions
```bash
sudo chmod +x /usr/sbin/sendmail
```
