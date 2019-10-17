1.  Setup your own lab within vmware/virtualbox
      - Use CentOS 7 or download free copy of RHEL from redhat

2.  Create another vm. Now setup the following servers
      - Setup own LDAP server https://goo.gl/6zSgHC
      - Setup own NFS server https://goo.gl/8W6KU8
3.  Don't rely on gui, Use SSH as soon as is possible. 
4.  For managing firewall, don't rely on gui also. Use firewall-cmd command
5.  Know how to use man/info/help/locate/find/rpm -qd command
6.  Understand linux filesystems and how to work with lvm
7.  Understand how to modify the filesystem (extend, reduce/resize commands). For example: extend the size (by using logical extent or specific size)reduce size of partition/logical volume, resize to exact size without hampering the files on the filesystem, check the filesystem health, labelling etc. 
8.  Understand logical extents. https://goo.gl/wTyB3R
9.  Be familiar with RHCSA objectives.
10. Use multiple ssh windows and monitor logs for errors(audit.log, messages and journalctl -xf)
11. Watch Sander van Vugt's advice on RHCSA exam https://www.youtube.com/watch?v=tok9qimRw6k
12. Every service must servive reboot. Every change must be persistent. Reboot and check if everything is working or not

14. If you forgot how to setup cronjob, just look inside /etc/crontab file
15. Give extra care on:
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

 16. Instead of memorizing big command for managing virtualization, simply remember the following group command:
     #yum groups install "Virtualization Hypervisor" "Virtualization Client" "Virtualization Tools"  "Virtualization Platform"
     Forgot that command also? No worries! just execute: #yum group list hidden
 17. If there are any filesystem related task, try to solve that task at first. Then reboot to see if your system boot properly or not.
 18. Give extra attention on time
 19. Always go through and **practice** each RHCSA objectives unless you feel absolutely ready
 20. Don't consult guide if you forgot anything. Just learn to use man/info/help/locate/find/rpm -qd command

# Advice
  - Use nmcli to setup and manage the network config
  - Install useful packages first. For example: yum-utils, bash-completion, setroubleshoot-server etc
  - Make sure that you know how to manually create a new repository
  - During the test, relax, don't hurry. If you finish early, reboot the machine couples of time and reveiw the questions.
  
  
  Good luck!

