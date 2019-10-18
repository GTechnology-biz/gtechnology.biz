---
layout: post
title: RHCSA Tips
---

- Setup your own lab within vmware/virtualbox
  - Use CentOS 7 or download free copy of RHEL from redhat

- Create another vm. Now setup the following servers
  - Setup own LDAP server [https://goo.gl/6zSgHC](https://goo.gl/6zSgHC)
  - Setup own NFS server [https://goo.gl/8W6KU8](https://goo.gl/8W6KU8)
- Don't rely on gui, Use SSH as soon as is possible. 
- For managing firewall, don't rely on gui also. Use firewall-cmd command
- Know how to use man/info/help/locate/find/rpm -qd command
- Understand linux filesystems and how to work with lvm
- Understand how to modify the filesystem (extend, reduce/resize commands). For example: extend the size (by using logical extent or specific size)reduce size of partition/logical volume, resize to exact size without hampering the files on the filesystem, check the filesystem health, labelling etc. 
- Understand logical extents. [https://goo.gl/wTyB3R](https://goo.gl/wTyB3R)
- Be familiar with RHCSA objectives.
- Use multiple ssh windows and monitor logs for errors(audit.log, messages and journalctl -xf)
- Watch Sander van Vugt's advice on RHCSA exam [https://www.youtube.com/watch?v=tok9qimRw6k](https://www.youtube.com/watch?v=tok9qimRw6k)
- Every service must servive reboot. Every change must be persistent. Reboot and check if everything is working or not

- If you forgot how to setup cronjob, just look inside /etc/crontab file
- Give extra care on:
  - File system partitioning (Use UUID when you add your file system in /etc/fstab for persistency)
  - ACL
  - firewall-cmd (with --permanent option)
  - setuid/setgid
  - File/folder permission
  - Selinux
   - Seboolean (with -P option)
  - breaking root password
  - ldap
  - autofs
  - nfs
  - network setup
  - etc

- Instead of memorizing big command for managing virtualization, simply remember the following group command:
     #yum groups install "Virtualization Hypervisor" "Virtualization Client" "Virtualization Tools"  "Virtualization Platform"
     Forgot that command also? No worries! just execute: #yum group list hidden
 - If there are any filesystem related task, try to solve that task at first. Then reboot to see if your system boot properly or not.
 - Give extra attention on time
 - Always go through and **practice** each RHCSA objectives unless you feel absolutely ready
 - Don't consult guide if you forgot anything. Just learn to use man/info/help/locate/find/rpm -qd command

# Advice
- Use nmcli to setup and manage the network config
- Install useful packages first. For example: yum-utils, bash-completion, setroubleshoot-server etc
- Make sure that you know how to manually create a new repository
- During the test, relax, don't hurry. If you finish early, reboot the machine couples of time and reveiw the questions.
  
  
  Good luck!

