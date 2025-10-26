# Firewall-configuration
Configured Windows Defender Firewall using its graphical interface. Viewed inbound rules, created a rule to block Telnet (port 23), tested to confirm the connection was denied, and then removed the rule to restore default settings, demonstrating GUI-based firewall control effectively.

<h1 align="center"> Firewall Configuration Using GUI Tools </h1>

<p align="center">
  <b>Author:</b> Vistruti Mahajan  
  <b>Domain:</b> Cybersecurity | <b>Practical:</b> Firewall Configuration  
</p>



Objective
To configure and manage firewall settings using **graphical tools**, including adding and removing rules, blocking specific ports, and allowing secure services.


Tools & Platforms

| Platform | Tool Used | Purpose |
|-----------|------------|----------|
| 🪟 Windows | **Windows Defender Firewall with Advanced Security** | Manage inbound/outbound traffic via GUI |
| 🐧 Linux | **GUFW (Graphical Uncomplicated Firewall)** | Configure firewall rules in a user-friendly interface |
| 🌐 Telnet / SSH | For testing blocked or allowed ports | Verify rule effectiveness |



Procedure

"Windows Firewall (GUI Method)"

Step 1 — Open the Firewall Tool
1. Press **Windows + R**, type `wf.msc`, and press **Enter**  
   *(or go to Control Panel → System and Security → Windows Defender Firewall → Advanced Settings)*  
2. The **Windows Defender Firewall with Advanced Security** window appears.

Step 2 — View Existing Rules
- Click on **Inbound Rules** or **Outbound Rules** in the left pane.  
- The list of existing firewall rules will be displayed, showing their name, port, and action (Allow/Block).

Step 3 — Add a Rule to Block a Specific Port (Example: Port 23 - Telnet)
1. In the left pane, select **Inbound Rules**.  
2. On the right side, click **New Rule...**  
3. Choose **Port → TCP → Specific Local Port: 23 → Next**  
4. Select **Block the Connection → Next**  
5. Choose the network types (Domain, Private, Public) → **Next**  
6. Name the rule (e.g., “Block Telnet Port 23”) → **Finish**

A new rule now appears in the list showing the block on port 23.

Step 4 — Test the Rule
- Try connecting to the blocked port using any Telnet or network testing tool.  
- The connection should **fail**, confirming that the rule is working.

Step 5 — Allow a Secure Connection (Optional)
1. Click **New Rule...** again → choose **Port → TCP → Specific Local Port: 22 → Allow the Connection**  
2. Name it “Allow SSH Port 22” → Finish.

Step 6 — Remove the Block Rule
- Select the **Block Telnet Port 23** rule from the list → **Right-click → Delete**  
- Confirm deletion to restore the original firewall configuration.



Linux Firewall (GUFW GUI) if using linux.

> GUFW is the graphical interface for the Uncomplicated Firewall (UFW) — designed to make Linux firewall management easy.

Step 1 — Open GUFW
1. Go to "Applications → Settings → Firewall Configuration"  
   "(If not installed, run `sudo apt install gufw` in terminal first.)"  
2. The "GUFW window" opens showing the firewall status.

Step 2 — Enable Firewall
- Toggle the Status switch "ON" to activate the firewall.

Step 3 — View Existing Rules
- Under the Rules tab, view all current Allowed and Denied connections.

Step 4 — Block a Specific Port (e.g., 23 for Telnet)
1. Click + (Add Rule)
2. In the Preconfigured or Simple tab:  
   - Policy: "Deny"  
   - Direction: "In"  
   - Protocol: "TCP"  
   - Port:"23"  
3. Click "Add" → The new blocking rule appears in the list.

Step 6 — Test the Rules
- Try connecting using a Telnet.  
  - Port **23** should be blocked.  

Step 7 — Remove the Block Rule
- Select the Telnet (Port 23) rule → Click the trash icon (🗑️) to delete it.  
- Firewall reverts to its original state.


~ Observation Table

| Action | Tool | Expected Output | Verified |
|--------|------|-----------------|-----------|
| View firewall rules | GUI | Shows all existing inbound/outbound rules | ✅ |
| Block Port 23 | GUI | Connection to port 23 denied | ✅ |
| Remove Rule | GUI | Firewall restored | ✅ |


~ Result
Firewall successfully configured using **graphical tools** on both **Windows** and **Linux**.  
Ports were blocked and allowed as per security requirements, demonstrating GUI-based rule management and testing.



~ Key Learnings
- Visual understanding of inbound/outbound network traffic control  
- GUI-based firewall management (Windows & GUFW)  
- Blocking and allowing ports securely  
- Testing and verifying firewall configurations effectively  

Performed By
Vistruti Mahajan  
Firewall Configuration using Tools. 

<p align="center">
   <b>“A secure system is one that controls its doors wisely.”</b>
</p>

