# simple_backup
simple_backup.py for pwnagotchi (Jay 2.9.5.3)

Automated backup solution for Pwnagotchi configurations and data.

Installation
Copy simple_backup.py to /usr/local/share/pwnagotchi/custom-plugins/
Configuration
```
main.plugins.simple_backup.enabled = true
main.plugins.simple_backup.interval_hours = 1
main.plugins.simple_backup.backup_path = "/home/pi/backups"
main.plugins.simple_backup.max_backups = 5
main.plugins.simple_backup.compress = true
main.plugins.simple_backup.backup_on_boot = true
```

Options

enabled - Enable/disable plugin (default: true)
interval_hours - Backup interval in hours (default: 1)
backup_path - Directory for backups (default: "/home/pi/backups")
max_backups - Maximum number of backups to keep (default: 5)
compress - Use gzip compression (default: true)
backup_on_boot - Create backup on startup (default: true)


Features

Automated scheduled backups
Automatic cleanup of old backups (keeps newest files)
Manual trigger via webhook: http://pwnagotchi:8080/plugins/simple_backup/backup


Backed up items

/etc/pwnagotchi/config.toml
/etc/pwnagotchi/ keys and fingerprint
/etc/ssh/ configurations
/home/pi/handshakes
/root/ configurations
/usr/local/share/pwnagotchi/custom-plugins
Various dotfiles and settings
