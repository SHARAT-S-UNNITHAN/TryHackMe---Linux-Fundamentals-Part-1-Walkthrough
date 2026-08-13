# TryHackMe - Linux Fundamentals Part 1 - Complete Walkthrough

**Room:** [Linux Fundamentals Part 1](https://tryhackme.com/room/linuxfundamentalspart1)
**Completed by:** Sharat S Unnithan
**Platform:** TryHackMe
**Category:** Cyber Security 101
**Difficulty:** Easy
**Time:** ~15 minutes
**Status:** ✅ Completed (100%)

---

## 📋 Room Overview

This room introduces the fundamentals of Linux, covering essential commands and concepts needed for cybersecurity. Linux powers websites, car entertainment systems, point of sale systems, critical infrastructure, and phones.

### Key Points
- Linux is more lightweight than Windows
- Used in websites, cars, PoS systems, traffic lights, phones
- Critical for cybersecurity professionals
- Terminal (CLI) is essential for cybersecurity work

---

## 📁 File Structure Overview

### Home Directory (/home/tryhackme)
```
home/tryhackme/
├── access.log          # Contains THM{ACCESS} flag
├── folder1/
│   ├── access.log      # Additional log file
│   └── password.txt    # Contains: password123
├── folder2/
├── folder3/
└── folder4/
```

---

## 📚 Task 1: Introduction

### Learning Objectives
- Understand where Linux is used in everyday life
- Deploy your first Linux machine

### Answer
✅ I've deployed my machine and am ready to go

---

## 📚 Task 2: Who Are You On This Machine?

### Commands Learned

| Command | Description | Example |
|---------|-------------|---------|
| `whoami` | Shows current user | `whoami` |
| `echo` | Output text | `echo "text"` |

### Practical Examples
```bash
# Check current user
whoami
# Output: tryhackme

# Output text
echo "TryHackMe"
# Output: TryHackMe

# Output multiple words
echo "hello world"
# Output: hello world
```

### Answers
| Question | Answer |
|----------|--------|
| What command would we use to find out who we are on the system? | `whoami` |
| What command would we use to output some text? | `echo` |

---

## 📚 Task 3: Move Around Without Ever Touching a Mouse

### Navigation Commands

| Command | Description | Example |
|---------|-------------|---------|
| `ls` | List directory contents | `ls` |
| `cd` | Change directory | `cd folder1` |
| `cat` | View file contents | `cat file.txt` |
| `pwd` | Print working directory | `pwd` |

### Step-by-Step Solution

1. **List current directory:**
```bash
ls
# Output: access.log  folder1  folder2  folder3  folder4
```

2. **Enter folder1:**
```bash
cd folder1
ls
# Output: access.log  password.txt
```

3. **Read the password.txt file:**
```bash
cat password.txt
# Output: password123
```

### Answers
| Question | Answer |
|----------|--------|
| Run ls in the current folder. How many folders are there? | `4` |
| One of those folders contains a file. Which folder is it? | `folder1` |
| Use cat to read the file within this folder. What does it say? | `password123` |

---

## 📚 Task 4: Never Search for Things by Hand Again

### Search Commands

| Command | Description | Example |
|---------|-------------|---------|
| `find` | Search for files by name | `find -name passwords.txt` |
| `grep` | Search inside files for text | `grep "password123" file.txt` |

### Step-by-Step Solution

1. **Navigate to home directory:**
```bash
cd /home/tryhackme
```

2. **Search for THM flag in access.log:**
```bash
grep "THM" access.log
# Output: THM{ACCESS}
```

### Answer
| Question | Answer |
|----------|--------|
| After using grep THM access.log a flag was found. What is the flag? | `THM{ACCESS}` |

---

## 📚 Task 5: Combine Commands and Capture Their Output

### Operators

| Operator | Description | Example |
|----------|-------------|---------|
| `&` | Run in background | `command &` |
| `&&` | Run sequentially | `command1 && command2` |
| `>` | Redirect (overwrite) | `echo "text" > file` |
| `>>` | Redirect (append) | `echo "text" >> file` |

### Practical Examples
```bash
# Create file with content
echo "hey" > welcome
cat welcome
# Output: hey

# Append to file
echo "there" >> welcome
cat welcome
# Output: hey
#         there

# Run commands sequentially
cd folder1 && cat password.txt
```

### Answers
| Question | Answer |
|----------|--------|
| What operator waits for the first command to finish before running the next command? | `&&` |
| What redirector allows us to save the output of a command without overwriting the contents of a file? | `>>` |

---

## 🎯 Complete Commands Cheatsheet

### Basic Commands
```bash
whoami              # Display current user
echo "text"         # Display text
pwd                 # Show current directory
ls                  # List files
ls -la              # List all files (including hidden)
cd <directory>      # Change directory
cd ..              # Go up one level
cd ~               # Go to home directory
cat <file>         # View file contents
```

### Search Commands
```bash
grep "pattern" file    # Search in file
grep -r "pattern" dir  # Search recursively
find . -name "*.txt"   # Find files by extension
find / -name "file"    # Find file in system
```

### Operators and Redirection
```bash
command1 && command2   # Run command2 if command1 succeeds
command1 &             # Run command1 in background
command > file         # Redirect output (overwrite)
command >> file        # Redirect output (append)
command < file         # Take input from file
command1 | command2    # Pipe output to another command
```

---

## 🔍 Key Findings

- `folder1` contains both `access.log` and `password.txt`
- `password.txt` contains: `password123`
- Main `access.log` in home directory contains flag: `THM{ACCESS}`

---

## 💡 Key Takeaways

1. **Linux is everywhere** - from servers to embedded systems
2. **Terminal is essential** - most cybersecurity work happens in CLI
3. **Navigation is fundamental** - ls, cd, cat, pwd are core commands
4. **Search efficiently** - grep and find save time
5. **Combine commands** - operators make you more productive

---

## 🚀 Next Steps

- [ ] Practice these commands regularly
- [ ] Complete Linux Fundamentals Part 2
- [ ] Explore more advanced Linux topics
- [ ] Try bash scripting
- [ ] Learn about file permissions

---

## 📊 Room Statistics
- **Room Progress:** 100% ✅
- **Questions Answered:** 9/9
- **Time Completed:** ~15 minutes
- **Difficulty:** Easy

---

## 🔗 Resources
- [TryHackMe Room](https://tryhackme.com/room/linuxfundamentalspart1)
- [Linux Command Reference](https://linux.die.net/)
- [Bash Cheatsheet](https://devhints.io/bash)

---

**Completed by:** Sharat S Unnithan  
**GitHub:** [SHARAT-S-UNNITHAN](https://github.com/SHARAT-S-UNNITHAN)  
**Date:** Aug 13 2026
**Room Link:** [Linux Fundamentals Part 1](https://tryhackme.com/room/linuxfundamentalspart1)

---

*Happy Hacking! 🎉*
