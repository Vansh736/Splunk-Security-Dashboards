
Total SSH brute force attacks:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json"
| stats count AS "Total SSH brute force attacks"


Successfull login:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Successful SSH Login"
| stats count AS "Successful Logins"


Failed logins:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Failed SSH Login"
| stats count AS "Failed Logins"


Invalid User Attempts:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Multiple Failed Authentication Attempts"
| stats count AS "Invalid User Attempts"


Failed logins by username:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Failed SSH Login" | top username


Brute Force attack with geo-location:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Multiple Failed Authentication Attempts" 
| table id.orig_h
| iplocation id.orig_h
| stats count by Country
| geom geo_countries featureIdField="Country"


Possible brute Force:

source="ssh_logs_new.json" host="LinuxServer" sourcetype="_json" event_type="Multiple Failed Authentication Attempts" | top id.orig_h


