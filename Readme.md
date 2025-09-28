# Task 4: Setup and Use a Firewall on Windows/Linux

## Objective
Configure and test basic firewall rules to allow or block traffic.

## Tools Used
- Windows Defender Firewall (Advanced Settings)
- UFW (Uncomplicated Firewall) on Ubuntu Linux

---

## Windows Firewall Configuration

### 1. Open Firewall Tool
- Run `wf.msc` or go to Control Panel → System and Security → Windows Defender Firewall → Advanced Settings

### 2. List Current Rules
- Navigate to **Inbound Rules** and **Outbound Rules**

### 3. Block Port 23 (Telnet)
- Inbound Rules → New Rule → Port → TCP → 23 → Block → All Profiles → Name: `Block Telnet`

### 4. Test
- Run `telnet localhost 23` → Connection should fail

### 5. Remove Rule
- Right-click `Block Telnet` → Delete

---

## Linux Firewall (UFW)

### 1. Enable UFW
```bash
sudo apt install ufw
sudo ufw enable
