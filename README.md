# 🐧 Ubuntu CLI Cheat Sheet

A quick reference for essential Ubuntu command-line operations, including system monitoring, networking, file management, user management, and more.

---

## 📌 Table of Contents

1. 🖥️ System Information – Check system details and hardware info  
2. 📁 File & Directory Management – Manage files and directories  
3. ⚡ System Monitoring & Process Management – Monitor system performance and processes  
4. 🔒 File Permissions & Ownership – Manage file access rights  
5. 🔎 Searching & Finding Files – Find files and search within them  
6. 🔧 Service Management – Start, stop, and check system services  
7. 📦 Archiving & Compression – Compress and extract files  
8. 📝 Text Editing & Processing – Edit and view text files  
9. ⏰ Cron Jobs & Scheduling – Automate tasks on a schedule  
10. 📦 Package Management – Install, update, and remove software  
11. 🌐 Networking – Check network connections and IPs  
12. 🛡️ Firewall Management – Control network access with UFW  
13. 🔑 SSH & Remote Access – Access remote machines securely  
14. 👥 User & Group Management – Manage system users and groups  
15. 🚀 Ubuntu Pro & LXD – Use advanced Ubuntu services and containers  

---

## 🖥️ Ubuntu CLI Commands  

```bash
# 🖥️ System Information (Check system details and hardware info)
uname -a                     # Displays all system information  
hostnamectl                  # Shows current hostname and related details  
lscpu                        # Lists CPU architecture information  
timedatectl status           # Shows system time  
df -h                        # Displays disk usage in a human-readable format  
free -m                      # Shows free and used memory in MB  

# 📁 File & Directory Management (Manage files and directories)
ls                           # Lists files and directories  
pwd                          # Displays current directory path  
cd <directory>               # Changes directory  
mkdir <dirname>              # Creates a new directory  
touch <filename>             # Creates an empty file or updates the timestamp  
cp <source> <destination>    # Copies files from source to destination  
mv <source> <destination>    # Moves or renames files  
rm <filename>                # Deletes a file  

# ⚡ System Monitoring & Process Management (Monitor system performance and processes)
top                          # Displays real-time system processes  
htop                         # Interactive process viewer (needs installation)  
jobs                         # Displays background processes  
fg <job_number>              # Brings a background job to the foreground  
kill <process_id>            # Terminates a process  
journalctl -f                # Follows the system journal logs in real-time  
journalctl -u <unit_name>    # Displays logs for a specific systemd unit  

# 🔒 File Permissions & Ownership (Manage file access rights)
chmod [who][+/-][permissions] <file>  # Changes file permissions  
chmod u+x <file>                      # Makes a file executable  
chown [user]:[group] <file>           # Changes file owner and group  

# 🔎 Searching & Finding Files (Find files and search within them)
find [directory] -name <pattern>  # Finds files by name  
grep <pattern> <file>             # Searches for text in files  

# 🔧 Service Management (Start, stop, and check system services)
sudo systemctl start <service>   # Starts a service  
sudo systemctl stop <service>    # Stops a service  
sudo systemctl status <service>  # Checks service status  
sudo systemctl reload <service>  # Reloads service configuration without interruption  

# 📦 Archiving & Compression (Compress and extract files)
tar -czvf <name.tar.gz> [files]  # Compress files into .tar.gz  
tar -xvf <name.tar.[gz|bz|xz]>   # Extract a compressed tar archive  

# 📝 Text Editing & Processing (Edit and view text files)
nano <file>                      # Opens a file in the Nano text editor  
cat <file>                       # Displays file contents  
less <file>                      # Paginated file view  
head <file>                      # Shows first few lines of a file  
tail <file>                      # Shows last few lines of a file  
awk '{print}' <file>             # Prints every line in a file  

# ⏰ Cron Jobs & Scheduling (Automate tasks on a schedule)
crontab -e  # Edits cron jobs  
crontab -l  # Lists cron jobs  

# 📦 Package Management (Install, update, and remove software)
sudo apt update                        # Updates package lists  
sudo apt install <package>              # Installs a package  
sudo apt install -f --reinstall <package>  # Reinstalls a broken package  
sudo apt remove <package>               # Removes a package  
sudo apt purge <package>                # Removes package + configuration  

# 🌐 Networking (Check network connections and IPs)
ip addr show   # Displays network interfaces & IPs  
ping <host>    # Pings a host  
ss -l         # Shows listening sockets  

# 🛡️ Firewall Management (Control network access with UFW)
sudo ufw status                  # Displays firewall status  
sudo ufw enable                  # Enables firewall  
sudo ufw disable                 # Disables firewall  
sudo ufw allow <port/service>     # Allows traffic on a specific port  
sudo ufw deny <port/service>      # Denies traffic on a specific port  
sudo ufw delete allow/deny <port/service>  # Deletes an existing rule  

# 🔑 SSH & Remote Access (Access remote machines securely)
ssh <user@host>                     # Connects via SSH  
scp <source> <user@host>:<dest>      # Securely copies files remotely  

# 👥 User & Group Management (Manage system users and groups)
sudo adduser <username>       # Creates a new user  
sudo deluser <username>       # Deletes a user  
sudo passwd <username>        # Changes user password  

# 🚀 Ubuntu Pro & LXD (Use advanced Ubuntu services and containers)
sudo pro attach <token>         # Attaches machine to Ubuntu Pro  
sudo pro status                 # Displays Ubuntu Pro status  
sudo pro enable esm-infra       # Enables Extended Security Maintenance  
sudo pro enable livepatch       # Enables Livepatch service (kernel patching)  

lxd init                           # Initializes LXD  
lxc list                           # Lists running containers/VMs  
lxc launch ubuntu:22.04 <name>     # Creates a new container  
lxc exec <instance> -- bash        # Opens a shell inside a container
