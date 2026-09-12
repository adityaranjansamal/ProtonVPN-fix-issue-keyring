# ProtonVPN-fix-issue-keyring
Proton VPN relies on sqlite secrets that conflicts and overwrites default linux keyring such as gnome keyring data or kdewallet which causes unwanted keyring errors and popups to create new keyring on reboots. This file fixes the issue partially.
Add the keyring_linux.py to this directory:  
```bash
/usr/lib/python3.14/site-packages/proton/keyring_linux/core
```
And replace/rename the .py file here to .bak and then paste this file.  
What's Changed?  
Added 
```bash
 stored_data = stored_data.replace("\n", "\\n")
```
to line 67
