# 🚀 Day 03 - Shell Scripting for DevOps Automation

## 📌 Overview

In this task, I explored shell scripting fundamentals to automate repetitive system tasks. Shell scripting is a core DevOps skill used for automation, deployment, monitoring, and system management.

---

## 🧠 Why Shell Scripting in DevOps?

DevOps engineers use shell scripts to:
- Automate deployments
- Monitor system health
- Manage logs
- Reduce manual effort

---

## 🛠️ Basic Script Example

### 📄 Script: system_info.sh

```bash
#!/bin/bash

echo "===== System Information ====="
echo "User: $(whoami)"
echo "Current Date: $(date)"
echo "System Uptime:"
uptime
echo "Disk Usage:"
df -h
echo "Memory Usage:"
free -m

chmod +x system_info.sh
./system_info.sh


#!/bin/bash

SOURCE="/home/ec2-user/data"
DEST="/home/ec2-user/backup"

mkdir -p $DEST
cp -r $SOURCE/* $DEST/

echo "Backup completed successfully at $(date)"


mkdir devops-day04
cd devops-day04

nano system_info.sh
nano file_backup.sh

chmod +x *.sh
./system_info.sh
./file_backup.sh
