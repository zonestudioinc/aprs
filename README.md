#PHP API for APRS by UC6KFQ#

In class APRS released auth on APRS-servers and sending messages with current position.

##Methods in APRS-api##

**sendPosition($lat, $long, $comment)** - sending position to APRS servers

**sendMsgToCallSign($recipient, $msg)** - sending text-message to other CallSign - *in implementation*
 
 
##How Use##
 
 1) Open file **clientAprs.php**
 
 2) Set your **Callsign, Pass, Lat, Long, Comment** and save
 
 3) Run script: 
 
 ```
 php clientAprs.php
 ```
  
###For add to cron on Linux(CentOS):###
 
   1) Open cron config: 
   
   ```
   crontab -e
   ```
   
   2) add lines:
   
   ```
   
    SHELL=/bin/bash
    PATH=/sbin:/bin:/usr/sbin:/usr/bin
    MAILTO=root
    HOME=/
    
    # run-parts
    
    */15 * * * * /usr/bin/php /{path_to_script}/clientAprs.php
   
   ```
   
   *Send position every 15min*
   
   3) Restart cron:
   
   ```
   service crond restart
   ```
