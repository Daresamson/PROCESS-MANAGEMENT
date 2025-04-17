# PROCESS-MANAGEMENT
---

# 🧠 Linux Process Management  
**Project 12: Process Management**  
*By Dare Samson*

## 🎯 Objective
To learn how to manage processes in Linux, including how to start, stop, monitor, and change process priorities.

---

## ✅ Tasks Completed
![Screenshot (260)](https://github.com/user-attachments/assets/b93d55b6-df55-46d0-b47f-ddb1e61291b0)

### 1. Start a Background Process
I started a background process using the `sleep` command:

```bash
sleep 300 &
```

This allowed the process to run in the background without blocking the terminal.

---

### 2. List Running Processes
To list all active processes, I used:

```bash
ps aux
```

This showed details like PID, user, CPU usage, memory, and command.

---
![Screenshot (260)](https://github.com/user-attachments/assets/20439105-ae51-49d7-8e57-23a2a29bd9e0)

### 3. Kill a Process
I located the process ID (PID) of the `sleep` command:

```bash
ps aux | grep sleep
```

Then I killed it using:

```bash
kill <PID>
```

If the process had already completed, I confirmed it with the message:
```bash
[1]+  Done sleep 300
```

---
![Screenshot (262)](https://github.com/user-attachments/assets/8029b80d-4b25-4e87-8a9a-16553473d489)

### 4. Monitor System Resources
I used the `top` command to monitor system performance and view real-time running processes:

```bash
top
```

---
![Screenshot (264)](https://github.com/user-attachments/assets/e2b0afb9-c35c-465b-928c-8cb8c48a45ce)

### 5. Change Process Priority
I started another background process with a custom nice value:

```bash
nice -n 10 sleep 300 &
```

Then I attempted to change its priority using `renice`:

```bash
renice -n 5 -p <PID>
```

I encountered a `Permission denied` error as a non-root user. I resolved this by running:

```bash
sudo renice -n 5 -p <PID>
```
![Screenshot (265)](https://github.com/user-attachments/assets/ed7f377a-4d08-4a86-9411-7c921514b994)

This successfully updated the process's priority.

---

## 🚀 Outcome
I successfully:
- Managed background processes  
- Located and killed processes  
- Monitored real-time system usage  
- Adjusted process priority using `nice` and `renice`  

---
