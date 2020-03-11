ansible-playbook playbookName.yml --extra-vars 'ansible_user=user ansible_password=passwd'

el resultado del logrotate generado con el playbook 6 es similar a:
```

## CONTENT ADMINISTRATED BY SSMM-MF ANSIBLE PLAYBOOK. ALL CHANGES WILL BE LOST

  /var/log/messages-????????
  /var/log/boot.log-????????
  /var/log/dmesg-????????
  /var/log/cron-????????
  /var/log/maillog-????????
  /var/log/secure-????????
  /var/log/spooler-????????
  /var/log/httpd/access_log-????????
  /var/log/httpd/error_log-????????
  /var/log/btmp-????????
  /var/log/wtmp-????????
  {

rotate 1
compress
daily
dateext
dateformat -%Y-%m-%d.log

prerotate
     /usr/bin/find /var/log/ -name "messages-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "boot.log-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "dmesg-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "cron-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "maillog-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "secure-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "spooler-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/httpd/ -name "access_log-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/httpd/ -name "error_log-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "btmp-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "wtmp-????????*.gz" -type f -mtime +1 -exec rm -f {} \;
endscript

postrotate
     /usr/bin/find /var/log/ -name "messages-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "boot.log-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "dmesg-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "cron-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "maillog-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "secure-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "spooler-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/httpd/ -name "access_log-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/httpd/ -name "error_log-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "btmp-????????" -type f -size 0b -exec rm -f {} \;
     /usr/bin/find /var/log/ -name "wtmp-????????" -type f -size 0b -exec rm -f {} \;
endscript

   }


```




