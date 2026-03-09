Web traffic logs

source="apache_logs.json" host="webserver" sourcetype="_json" 
| stats count AS "Total Web Requests"



Successfull response

source="apache_logs.json" host="webserver" sourcetype="_json" status=200
| stats count AS "Successfull Response"


Client Errors

source="apache_logs.json" host="webserver" sourcetype="_json" 
| where status>=400 and status<500
| stats count AS "Client Errors"

Server errors

source="apache_logs.json" host="webserver" sourcetype="_json" 
| where status>500
| stats count AS "Server Errors"

Top Requested URIs

source="apache_logs.json" host="webserver" sourcetype="_json" 
| top uri

Top Users by IP Address

source="apache_logs.json" host="webserver" sourcetype="_json" 
| stats count AS "IP" by ip
