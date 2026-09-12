# ProtonVPN-fix-issue-keyring
Custom fix for Proton VPN that relies on sqlite secrets that conflicts and overwrites default linux keyring such as gnome keyring data or kdewallet. This file fixes the issue by not allowing overwrite priiority.
