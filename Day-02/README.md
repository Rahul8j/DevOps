# 🚀 Day 02 - Advanced Linux Commands for DevOps

## 📌 Overview
This task focuses on applying Linux commands in practical scenarios such as file manipulation, sorting, filtering, and comparison — essential for real-world DevOps operations.

---

## 🧠 Why This Matters in DevOps

In production environments, DevOps engineers frequently:
- Analyze logs
- Process files
- Debug issues
- Automate tasks

Mastering command-line utilities enables efficient troubleshooting and automation.

---

## 📂 Tasks & Commands
```bash
1️⃣ Display File with Line Numbers
cat -n file.txt
2️⃣ View First & Last Lines
head -n 5 file.txt
tail -n 5 file.txt
3️⃣ Sort File Content
sort file.txttac file.txt
4️⃣ Reverse File Content
tac file.txt
5️⃣ Compare Files
comm file1.txt file2.txt
6️⃣ Count Words, Lines & Characters
wc file.txt
7️⃣ Create and Append Data
echo "DevOps" >> file.txt

🧪 Hands-on Implementation
mkdir devops-day03
cd devops-day03

echo -e "Apple\nMango\nBanana" > fruits.txt
echo -e "Banana\nOrange\nApple" > fruits2.txt

cat -n fruits.txt
head -n 2 fruits.txt
tail -n 2 fruits.txt
sort fruits.txt
tac fruits.txt

comm -12 <(sort fruits.txt) <(sort fruits2.txt)

wc fruits.txt
