##### Physical System Hardening

- Prevent others to access your servers
- Configure BIOS
  - Disable booting from CD/DVD and External Devices
  - Setup BIOS password
- Protect GRUB with password
- Disable USBs and Input Devices in OS-COnfiguration
  - `/etc/modprobe.d/no-usb`

##### Configure SSH connections

- Use key-based authentication instead of password-based authentication.
- Restrict SSH access from certain known IPs only
- Disable root login
  - Set `PermitRootLogin no` in `/etc/ssh/sshd_config`
- Set `Protocol 2` in `/etc/ssh/sshd_config`
- Users with the appropriately configured access level should be allowed to login

##### Disable Unnecessary Services & Ports

- Take down unnecessary open ports can quickly reduce the attack surface
- Lockdown Cronjobs
  - `/etc/cron.allow` and `/etc/cron.deny`

##### Activate Firewall

- Restrict access to Linux's services
  - Define policies
- Block unwanted connections
  - Zero Trust network

#### Strong Password Policies

- At least 18 characters that include lowercases, Uppercases, Numbers and Special Characters

##### Remove Unnecessary Packages

- Minimize Packages to Minimize Vulnerability
  - `chkconfig`

##### Keep Kernel and Packages Updated

##### Disable ICMP (or Limit Access)

- Ping sweep (to prevent identify hosts on a network)
- Ping flood (to prevent ICMP flood attack)
- ...

##### Logging and Auditing

- Detect any attempted intrusions
- Help to inspect the occurred breach

##### Turn Off IPv6

- To reduce attack surface
  - `/etc/sysconfig/network`

##### Separate Disk Partitions

- Keep partitions separated and grouped. It can helps decrease the radius of any attack

##### Regular Backups

- An off-site backup of your server can help you quickly recover any lost machines due to intrusion or attack

##### Automated Threat and Compliance Monitoring Tools

- IPS / IDS
  - Snort
  - Suricata
  - ...
