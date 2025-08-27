
📞 Asterisk Audio Conference with Admin & User Roles

This project demonstrates how to set up a simple audio conferencing system in Asterisk using ConfBridge.
We configure two types of participants:

Normal Users (extension 600)

Admin Users (extension 601)

Admins have elevated privileges like muting users, kicking participants, and ending the conference.

🚀 Setup
1. Edit extensions.conf

Add the following inside your [internal] context:

[internal]

; Normal User Conference
exten => 600,1,Answer()
 same => n,ConfBridge(600,default_bridge,default_user)
 same => n,Hangup()

; Admin User Conference
exten => 601,1,Answer()
 same => n,ConfBridge(600,default_bridge,admin_user)
 same => n,Hangup()


600 → Normal participant (default_user)

601 → Admin participant (admin_user)

Both join the same conference room (600)

2. Edit confbridge.conf

Configure profiles for normal users and admins:

Configure profiles for normal users and admins:

[general]

[default_bridge]
type=bridge
record_conference=no

[default_user]
type=user
music_on_hold_when_empty=yes
marked=no

[admin_user]
type=user
admin=yes
marked=yes
end_conference=yes
kick_participants=yes

3. Reload Asterisk

Run the following inside the Asterisk CLI:

asterisk -rx "dialplan reload"
asterisk -rx "module reload app_confbridge.so"

🎯 Usage

Normal User dials 600 to join the conference.

Admin User dials 601 to join with admin privileges.

All users are placed in the same conference room (600).

Admin can mute/unmute, kick users, or end the conference.


