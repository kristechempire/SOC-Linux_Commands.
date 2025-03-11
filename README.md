# SOC Linux Command Cheat Sheet  

A collection of essential Linux commands for SOC analysts to analyze logs, monitor system activities, and investigate security incidents.  

## 1. Log Analysis  
- View system logs:  
  ```bash
  cat /var/log/syslog
  View authentication logs (for failed/successful logins):

cat /var/log/auth.log
Monitor logs in real-time:

tail -f /var/log/syslog
User Monitoring

List logged-in users:

who
Show user login history:

last

Check currently active user sessions:

w
3. Process & Network Monitoring

View running processes:

ps aux

Find a specific process:

ps aux | grep <process-name>

Show open network connections:

netstat -tulnp

Check active connections using ss:

ss -tulnp
4. File & Permission Analysis

Check file permissions:

ls -lah

Find files with SUID/SGID (potential privilege escalation risks):

find / -type f -perm -4000 2>/dev/null

Search for a specific keyword in logs:

grep "keyword" /var/log/syslog
5. System Information & Security Checks

Check system uptime:

uptime

Display system information:

uname -a

List all open ports:

sudo lsof -i -P -n

Identify failed SSH login attempts:

grep "Failed password" /var/log/auth.log



