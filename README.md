#idumzaes/cups_airprint

Built from arm64v8/ubuntu

##Create and run container with:

`docker run -d --name cups-airprint -e CUPSADMIN=admin -e CUPSPASSWORD=pass -v ~/cups-airprint/config:/config -v ~/cups-airprint/services:/services -p 631:631 idumzaes/cups_airprint`
