# 🚀 Day 05 - Shell Scripting with Conditions & Automation

## 📌 Overview

This task focuses on adding logic to shell scripts using conditions and loops. These concepts are essential for building intelligent automation in DevOps workflows.

---

## 🧠 Why This Matters in DevOps

DevOps engineers use scripting to:
- Automate decision-making
- Monitor system health
- Trigger alerts
- Handle failures in pipelines

---

## 🛠️ Conditional Script Example

### 📄 Script: check_disk.sh

```bash
#!/bin/bash

THRESHOLD=80
USAGE=$(df -h / | awk 'NR==2 {print $5}' | sed 's/%//')

if [ $USAGE -gt $THRESHOLD ]; then
  echo "⚠️ Disk usage is above threshold: $USAGE%"
else
  echo "✅ Disk usage is under control: $USAGE%"
fi

Loop Script Example

#!/bin/bash

USERS=("ec2-user" "ubuntu" "admin")

for user in "${USERS[@]}"
do
  if id "$user" &>/dev/null; then
    echo "✅ User $user exists"
  else
    echo "❌ User $user does not exist"
  fi
done



mkdir devops-day05
cd devops-day05

nano check_disk.sh
nano user_check.sh

chmod +x *.sh

./check_disk.sh
./user_check.sh
