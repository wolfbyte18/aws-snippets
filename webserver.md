Goal: Create a webserver which will serve the default Apache splash page. (For testing connectivity.)

Steps: When launching an EC2 instance, on the 2nd screen (after AMI selection) expand "Advanced", and enter this as user-data:

```
#!/bin/bash
yum update -y
yum install -y httpd
service httpd start
```

Machine will respond to TCP/80 and ICMP requests (firewalls, SGs, etc. permitting).
