# Cloud-Based-Audio-Conferencing-and-Contact-Center-Simulation
VoIP & Audio Conferencing Projects
Project 1: Basic VoIP Call Between Zoiper and JIST

Description:
This project demonstrates a simple VoIP call setup using Asterisk PBX. A user can make a call from Zoiper softphone to a JIST client.

Steps to Install and Setup:

Install Asterisk (on Linux):

sudo apt update
sudo apt install -y asterisk
sudo systemctl start asterisk
sudo systemctl enable asterisk


Install Zoiper (Softphone):

Download Zoiper from https://www.zoiper.com

Install and configure with the SIP account created in Asterisk.

Install JIST Client:

Follow the JIST installation instructions from its official repository or package.

Configure SIP account with Asterisk credentials.

Make a Call:

Open Zoiper and register with your SIP account.

Dial the SIP address or extension of the JIST client.

Verify the call connects successfully.

Folder/Files:

Basic Asterisk configuration files (sip.conf, extensions.conf) for this scenario are provided in the project folder.

Project 2: Audio Conferencing with Conference ID 600

Description:
This project demonstrates a multi-party conference setup in Asterisk.

Conference ID 600: Normal users join here.

Conference ID 601: Admin joins here.

Steps to Install and Setup:

Install Asterisk:
(Follow same steps as Project 1)

Configure Conference in Asterisk:

Use confbridge.conf to define rooms 600 and 601.

Assign normal users to 600 and admin user to 601.

Join Conference:

Normal user dials extension 600.

Admin dials extension 601.

Verify both users can communicate appropriately.

Additional Information:

More detailed configurations, dialplans, and scripts can be found in the conf_with_ID_600 folder.
