# Elevate_Labs_Internship_Task_4

Elevate Labs Internship Task 4

# 🔥 Setup and Use a Firewall on Linux (UFW)

## 🎯 Objective

Configure and test basic firewall rules on Kali Linux using **UFW (Uncomplicated Firewall)** to control inbound/outbound traffic and enhance system security.

---

## 🛠 Tools Used

* **Firewall Utility**: UFW (Uncomplicated Firewall)
* **Operating System**: Kali Linux 2025.2
* **Test Tool**: Telnet (for port connectivity verification)

---

## 🧾 Step-by-Step Instructions

### ✅ 1. Open Firewall Configuration Tool

Check firewall status:

```bash
sudo ufw status
```

If it's inactive, enable it:

```bash
sudo ufw enable
```

---

### 📄 2. List Current Firewall Rules

```bash
sudo ufw status verbose
```

---

### ⛔ 3. Add Rule to Block Inbound Port 23 (Telnet)

```bash
sudo ufw deny 23
```

---

### 🧪 4. Test the Rule by Attempting a Connection

Test connection:

```bash
telnet localhost 23
```

Expected result:

```
Trying 127.0.0.1...
telnet: Unable to connect to remote host: Connection refused
```

---

### 🔓 5. Add Rule to Allow SSH (Port 22)

```bash
sudo ufw allow 22
```

---

### ♻️ 6. Remove the Test Block Rule (Port 23)

```bash
sudo ufw delete deny 23
```

---

### 🔐 8. Firewall Filtering Summary

UFW filters traffic by defining **allow or deny rules** based on:

* Port numbers
* IP addresses
* Protocol types

UFW helps protect the system by:

* Denying unsolicited inbound connections
* Allowing only trusted services (e.g., SSH)
* Logging rejected connection attempts

---

## 📷 Screenshot

* `Firewall conf.png` – Documented commands and its output

---

## ✍️ Author

**Sanjai K**
Elevate Labs Intern | Aspiring Pentration Tester
