# AutomationZ Log Cleanup Scheduler

AutomationZ Log Cleanup Scheduler is a **GUI-based automation tool** designed to safely and automatically clean up log files (or any other files) on both **local machines** and **FTP-based servers**.

It is built for:
- DayZ server administrators
- Game server hosts
- VPS / dedicated server owners
- Website administrators
- Anyone who needs scheduled file cleanup without scripting

No mods required.  
No Git knowledge required.  
Just configure and run.

---

## 🚀 What This Tool Does

- Automatically deletes files from configured folders
- Works on:
  - Local folders (local mode)
  - Remote servers via FTP / FTPS
- Supports multiple cleanup jobs
- Supports file exclusion (blacklist)
- Supports folder exclusion
- Dry-Run mode for safe testing
- Manual execution or scheduled execution
- Full logging of all actions

---

## 🧠 Typical Use Case

1. Your server generates log files continuously
2. Log folders grow over time and waste disk space
3. Some log folders also contain important config files
4. You want to delete logs but **never touch configs**
5. This tool removes only what is allowed — automatically

---

## 📁 Folder Structure (auto-created)

After first launch:
AutomationZ_Log_Cleanup_Scheduler/
├─ app/
├─ config/
│ └─ log_cleanup_config.json
├─ logs/
├─ logs_cache/
├─ reports/
├─ state/
├─ run_windows.bat
├─ run_linux_mac.sh
└─ README.md

All folders are created automatically if missing.

---

## ▶️ How to Start

### Windows
Double-click:

### Linux / macOS
```bash
chmod +x run_linux_mac.sh
./run_linux_mac.sh

| Tab         | Purpose                        |
| ----------- | ------------------------------ |
| Dashboard   | Run jobs and control scheduler |
| Jobs        | Define what gets cleaned       |
| FTP Targets | Manage FTP servers             |
| Settings    | Global configuration           |
| Help        | Quick usage instructions       |

Each tab is explained in detail below.

---

# 🖼️ IMAGE-SPECIFIC README SECTIONS  
*(Use these directly **below each screenshot** on GitHub or Wiki)*

---
[![Log_Cleanup_Dashboard.png](https://i.postimg.cc/C1ZNQDHH/Log_Cleanup_Dashboard.png)](https://postimg.cc/HcgXJrNV)
## 🖼️ **Dashboard**  
[![Log_Cleanup_Dashboard.png](https://i.postimg.cc/C1ZNQDHH/Log_Cleanup_Dashboard.png)](https://postimg.cc/HcgXJrNV)

```markdown
## Dashboard

The Dashboard is the control center of the Log Cleanup Scheduler.

### Job Selector
Select which cleanup job you want to execute.

### Run Job Now
- Executes the selected job immediately
- Ignores scheduling
- Recommended for testing

### Start Scheduler
- Enables automatic execution of scheduled jobs
- Jobs will run based on their configured time and days

### Status Panel
Shows:
- Current time
- Scheduler state (RUNNING / STOPPED)
- Overview of scheduled jobs

### Quick Access Buttons
- Open Config Folder
- Open Logs Folder
- Open Config File

🖼️ Jobs Tab
[![Log_Cleanup_Jobs.png](https://i.postimg.cc/6370mRLV/Log_Cleanup_Jobs.png)](https://postimg.cc/JDLZysFt)
## Jobs

The Jobs tab defines **what**, **where**, and **when** files are deleted.

### Job List (Left)
Shows all defined cleanup jobs.

Indicators:
- `[ON]` = job enabled
- `[MANUAL]` = no schedule configured

Buttons:
- New – create a new job
- Delete – remove selected job
- Save Changes – store modifications

---

### Job Details (Right)

#### Job Name
A descriptive name, for example:
DayZ – Server Logs Cleanup


#### Mode
- `local` – clean local folders
- `ftp` – clean folders on a remote FTP server

---

### Local Folders (Local Mode)
One folder per line:

C:\DayZ\Server\Logs
C:\DayZ\profiles\logs

---

### FTP Target (FTP Mode)
Select an FTP server previously defined in **FTP Targets**.

---

### FTP Remote Folders
Remote paths, one per line:
/dayzstandalone/logs
/dayzstandalone/profiles/logs

---

### File Exclusion (Blacklist)
Files that will **never be deleted**.

Supports wildcards:
*.json
*.cfg
important.log

---

### Folder Exclusion
Folder names that are skipped entirely:
config
settings

---

### Dry Run Mode
- Enabled → no files are deleted (simulation only)
- Disabled → files are permanently removed

⚠️ Always test with Dry Run enabled first.

---

### Scheduling
- Set execution time (24h format)
- Select days of the week
- Disabled = manual execution only

🖼️ FTP Targets Tab
[![Log_Cleanup_FTP_Targets.png](https://i.postimg.cc/bJGTBbHQ/Log_Cleanup_FTP_Targets.png)](https://postimg.cc/WFvgDdy3)
## FTP Targets

FTP Targets define remote servers where cleanup jobs can run.

### FTP Target List
Buttons:
- New – add a new FTP server
- Delete – remove selected target
- Save Changes – store settings

---

### FTP Target Details
- Name – internal label
- Host – FTP hostname or IP
- Port – usually 21
- Username
- Password
- Use FTPS (TLS) – optional

Use **Test Connection** to verify access before using the target in jobs.

🖼️ Settings Tab
[![Log_Cleanup_Settings.png](https://i.postimg.cc/gJwDTRqV/Log_Cleanup_Settings.png)](https://postimg.cc/8JSMF7Yc)
## Settings

Global application settings.

### Scheduler Interval
How often the scheduler checks if a job should run.

### FTP Timeout
Maximum wait time for FTP operations.

### Save Settings
All changes are written to the configuration file immediately.
🧩 Part of AutomationZ Control Center
This tool is part of the AutomationZ Admin Toolkit:

- AutomationZ Uploader
- AutomationZ Scheduler
- AutomationZ Server Backup Scheduler
- AutomationZ Server Health
- AutomationZ Config Diff
- AutomationZ Admin Orchestrator
- AutomationZ Log Cleanup Scheduler

Together they form a complete server administration solution.

### 💚 Support the project

AutomationZ tools are built for server owners by a server owner.  
If these tools save you time or help your community, consider supporting development.

☕ Ko-fi: https://ko-fi.com/dannyvandenbrande  
💬 Discord: https://discord.gg/6g8EPES3BP  

Created by **Danny van den Brande**  
DayZ AutomationZ



