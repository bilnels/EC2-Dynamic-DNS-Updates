DNS Server and Dynamic Updates of DNS Records in VPC
-----------------------------------------------------
Unfortunately, the Amazon DNS server cannot resolve private DNS hostnames if your VPC's IP address range falls outside of the private IP addresses ranges specified by the RFC.

For this reason the reverse/forward IP addresses lookups fail with similar errors shown below:

~]$ hostname -f
hostname: Unknown host

A workaround in this would be to have/create a designate DNS sever(bind) in your VPC  to do forward and reverse dns lookups within the VPC.
While dynamically updating the DNS records using a script during instance Launch.

