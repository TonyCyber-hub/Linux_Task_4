# COMMANDS.md

Command reference derived from the supplied lab instructions. Run commands only when performing the corresponding activity; commands involving `sudo`, users, networking configuration, or process termination may require appropriate privileges.

## Activity 1 — Navigation & File Management

```bash
mkdir linux_lab
cd linux_lab
mkdir docs scripts
touch readme.txt notes.txt script.sh
echo "Welcome to Linux Practice" > readme.txt
cp readme.txt docs/
mv notes.txt docs/
rm script.sh
tree
# or:
ls -R
```

## Activity 2 — File Viewing & Editing

```bash
nano readme.txt
head -n 3 readme.txt
tail -n 2 readme.txt
wc readme.txt
grep "Linux" readme.txt
```

Inside `readme.txt`, add your name and write the functions of Kernel, FHS, and Shell as required by the lab.

## Activity 3 — Permissions & Ownership

```bash
touch secure.txt
chmod 640 secure.txt
chmod 777 secure.txt
sudo useradd student2
sudo chown student2 secure.txt
ls -l secure.txt
```

The first permission state requested by the lab is owner read/write, group read-only, and others with no permissions (`640`). The lab then explicitly asks to change the file to `777`.

## Activity 4 — Archiving & Compression

```bash
mkdir backup_test
touch backup_test/file1.txt backup_test/file2.txt backup_test/file3.txt
tar -cf backup.tar backup_test
gzip backup.tar
mkdir restore_test
tar -xzf backup.tar.gz -C restore_test
ls -R restore_test
```

## Activity 5 — Process Management

```bash
sleep 300 &
jobs
fg
# After identifying the process PID:
kill <PID>
ps aux | grep sleep
top
```

`fg` brings the background job to the foreground. Because `sleep 300` then occupies the terminal, stop/interrupt it as appropriate before continuing to the PID-based termination step.

## Activity 6 — Networking Basics

```bash
ip a
ping google.com -c 4
ss -tulnp
hostname
sudo nano /etc/hosts
# Add:
# 127.0.0.1 testsite.local
ping testsite.local
```

## Activity 7 — Searching & Finding

```bash
find / -name readme.txt 2>/dev/null
grep "Linux" docs/*.txt
find . -type f -mtime -1
find ~ -type f -name "*.txt" | wc -l
```

## Activity 8 — Package Management (Debian/Ubuntu-based)

```bash
sudo apt update
sudo apt install tree
tree --version
sudo apt remove tree
dpkg -l > packages.txt
```

## Activity 9 — Scripting Basics

```bash
chmod +x hello.sh
./hello.sh
```

The script should display `Hello, Linux World!`, the current date/time using `date`, and the current working directory using `pwd`.

## Activity 10 — System Monitoring & Logs

```bash
df -h
free -h
tail -n 10 /var/log/syslog
# or, where applicable:
tail -n 10 /var/log/messages
uptime
who
lscpu
```
