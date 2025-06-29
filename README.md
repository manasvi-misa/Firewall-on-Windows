#  Task 4: Setup and Use a Firewall on Windows

##  Objective
Configure and test basic firewall rules to allow or block specific traffic using **Windows Defender Firewall with Advanced Security**.

---

##  Steps Performed

### 1. Opened Firewall Configuration
- Accessed via `wf.msc` (Run dialog) or through:
  `Control Panel → System and Security → Windows Defender Firewall → Advanced Settings`

### 2. Listed Current Inbound Rules
- Navigated to `Inbound Rules` section.

### 3. Created a New Rule to Block Port 23 (Telnet)
- **Type:** Port  
- **Protocol:** TCP  
- **Port:** 23  
- **Action:** Block the connection  
- **Profile:** Domain, Private, Public  
- **Rule Name:** `Telnet rule`

### 4. Tested the Rule
- Attempted `telnet localhost 23` in Command Prompt.
- Telnet was not installed (`'telnet' is not recognized...`) — expected on default Windows installs.
- Rule successfully shown as **Enabled + Block + Port 23** in Firewall rule list.

### 5. (Optional) Rule Removal
- Right-clicked the rule → Chose **Delete** or **Disable**.

---

##  Screenshot
- Attached screenshot: `Windows Firewall with Advanced Security` showing:
  - `Telnet rule` (Action: Block, Protocol: TCP, Port: 23)

---

##  Firewall Traffic Filtering Summary
Windows Firewall filters packets based on defined rules. It inspects data by:
- Source/destination IPs
- Protocols and ports
- Application context  
This controls access to system resources and protects against unauthorized traffic.
