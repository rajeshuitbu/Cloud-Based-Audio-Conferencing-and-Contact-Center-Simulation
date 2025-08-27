# VoIP & Audio Conferencing Projects

This repository contains two VoIP/Asterisk-based projects demonstrating basic calling and multi-party audio conferencing.

---

## Project 1: Basic VoIP Call Between Zoiper and JIST

**Description:**  
This project demonstrates a simple VoIP call setup using Asterisk PBX. A user can make a call from **Zoiper softphone** to a **JIST client**.

**Installation & Setup:**

1. **Install Asterisk (Linux):**
   ```bash
   sudo apt update
   sudo apt install -y asterisk
   sudo systemctl start asterisk
   sudo systemctl enable asterisk
Install Zoiper Softphone:

Download Zoiper from https://www.zoiper.com

Install and configure with the SIP account created in Asterisk.

Install JIST Client:

Follow official JIST installation instructions.

Configure SIP account with Asterisk credentials.

Make a Call:

Open Zoiper and register using your SIP account.

Dial the SIP address or extension of the JIST client.

Ensure the call connects successfully.

Files & Configuration:

Asterisk configuration files (sip.conf, extensions.conf) for this scenario are included in the project folder.

Project 2: Audio Conferencing with Conference ID 600

Description:
This project demonstrates a multi-party audio conference using Asterisk ConfBridge:

Conference ID 600: Normal users join here.

Conference ID 601: Admin joins here.

Installation & Setup:

Install Asterisk:
(Same steps as Project 1)

Configure Conference in Asterisk:

Edit confbridge.conf to define rooms 600 (normal users) and 601 (admin).

Ensure proper roles and privileges are set for each room.

Join the Conference:

Normal user dials extension 600.

Admin dials extension 601.

Verify communication between users and admin.

Additional Information:

Detailed configurations, dialplans, and scripts are available in the conf_with_ID_600 folder.
