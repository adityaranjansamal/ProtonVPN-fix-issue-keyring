# ProtonVPN-fix-issue-keyring
Custom fix for Proton VPN that relies on sqlite secrets that conflicts and overwrites default linux keyring such as gnome keyring data or kdewallet. This file fixes the issue by not allowing overwrite priiority.  
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
