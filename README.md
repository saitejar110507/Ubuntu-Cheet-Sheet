# 🐧 Ubuntu CLI Cheat Sheet  

A **quick reference** for essential **Ubuntu command-line operations**, including **file management, system monitoring, networking, user management, and more**.  

## 📌 Table of Contents  
1. [🖥️ System Information](#-system-information) – **Check system details and hardware info**  
2. [📁 File & Directory Management](#-file--directory-management) – **Manage files and directories**  
3. [⚡ System Monitoring & Process Management](#-system-monitoring--process-management) – **Monitor system performance and processes**  
4. [🔒 File Permissions & Ownership](#-file-permissions--ownership) – **Manage file access rights**  
5. [🔎 Searching & Finding Files](#-searching--finding-files) – **Find files and search within them**  
6. [🔧 Service Management](#-service-management) – **Start, stop, and check system services**  
7. [📦 Archiving & Compression](#-archiving--compression) – **Compress and extract files**  
8. [📝 Text Editing & Processing](#-text-editing--processing) – **Edit and view text files**  
9. [⏰ Cron Jobs & Scheduling](#-cron-jobs--scheduling) – **Automate tasks on a schedule**  
10. [📦 Package Management](#-package-management) – **Install, update, and remove software**  
11. [🌐 Networking](#-networking) – **Check network connections and IPs**  
12. [🛡️ Firewall Management](#-firewall-management) – **Control network access with UFW**  
13. [🔑 SSH & Remote Access](#-ssh--remote-access) – **Access remote machines securely**  
14. [👥 User & Group Management](#-user--group-management) – **Manage system users and groups**  
15. [🚀 Ubuntu Pro & LXD](#-ubuntu-pro--lxd) – **Use advanced Ubuntu services and containers**  

---

## 🖥️ System Information *(Check system details and hardware info)*  

uname -a                      # Displays all system information  
hostnamectl                   # Shows current hostname details  
lscpu                          # Lists CPU architecture information  
timedatectl status            # Displays system time  
df -h                          # Shows disk usage in human-readable format  
free -m                        # Displays free and used memory in MB

** 📁 File & Directory Management (Manage files and directories)

ls                             # Lists files and directories  
touch <filename>               # Creates an empty file  
cp <source> <destination>      # Copies files  
mv <source> <destination>      # Moves or renames files  
rm <filename>                  # Deletes a file  
mkdir <dirname>                # Creates a new directory  
pwd                            # Displays current directory path  
cd <directory>                 # Changes directory

** ⚡ System Monitoring & Process Management (Monitor system performance and processes)

top                            # Displays real-time system processes  
htop                           # Interactive process viewer (needs installation)  
kill <process_id>              # Terminates a process  
jobs                           # Displays background processes  
fg <job_number>                # Brings a background job to the foreground

** 🔒 File Permissions & Ownership (Manage file access rights)

chmod u+x <file>               # Makes a file executable  
chown [user]:[group] <file>    # Changes file owner and group

** 🔎 Searching & Finding Files (Find files and search within them)

find [directory] -name <pattern>   # Finds files by name  
grep <pattern> <file>              # Searches for text in files

** 🔧 Service Management (Start, stop, and check system services)

sudo systemctl start <service>  # Starts a service  
sudo systemctl stop <service>   # Stops a service  
sudo systemctl status <service> # Checks service status

** 📦 Archiving & Compression (Compress and extract files)

tar -czvf <name.tar.gz> [files]  # Compress files into .tar.gz  
tar -xvf <name.tar.gz>           # Extract a .tar.gz archive

** 📝 Text Editing & Processing (Edit and view text files)

nano <file>                      # Opens a file in Nano editor  
cat <file>                       # Displays file contents  
less <file>                      # Paginated file view  
head <file>                      # Shows first few lines of a file  
tail <file>                      # Shows last few lines of a file

** ⏰ Cron Jobs & Scheduling (Automate tasks on a schedule)

crontab -e   # Edits cron jobs  
crontab -l   # Lists cron jobs

** 📦 Package Management (Install, update, and remove software)

APT (Debian-based)

sudo apt update                   # Updates package lists  
sudo apt install <package>         # Installs a package  
sudo apt remove <package>          # Removes a package

Snap (Canonical-based)

snap find <package>                 # Searches for Snap packages  
sudo snap install <snap_name>        # Installs a Snap package

** 🌐 Networking (Check network connections and IPs)

ip addr show   # Displays network interfaces & IPs  
ping <host>    # Pings a host

** 🛡️ Firewall Management (Control network access with UFW)

sudo ufw status                 # Shows firewall status  
sudo ufw enable                 # Enables firewall  
sudo ufw allow <port/service>    # Allows traffic on a specific port

** 🔑 SSH & Remote Access (Access remote machines securely)

ssh <user@host>                     # Connects via SSH  
scp <source> <user@host>:<dest>      # Securely copies files remotely

** 👥 User & Group Management (Manage system users and groups)

User Management

sudo adduser <username>       # Creates a new user  
sudo deluser <username>       # Deletes a user  
sudo passwd <username>        # Changes user password

Group Management

id [username]                 # Displays user & group IDs  
groups [username]             # Shows user’s groups

🚀 Ubuntu Pro & LXD (Use advanced Ubuntu services and containers)

Ubuntu Pro

sudo pro attach <token>         # Attaches machine to Ubuntu Pro  
sudo pro status                 # Displays Ubuntu Pro status

LXD (Containers & VMs)

lxd init                        # Initializes LXD  
lxc list                        # Lists running containers/VMs  
lxc launch ubuntu:22.04 <name>  # Creates a new container
