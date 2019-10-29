# idumzaes/cups_airprint
CUPS Airprint Server built from arm64v8/alpine

## Setup
### Volumes:
`/config`: where the persistent printer configs will be stored.<br>
`/services`: where Avahi service files will be generated.
### Variables:
`CUPSADMIN`: the CUPS admin user you want created.<br>
`CUPSPASSWORD`: the password for the CUPS admin user.
### Ports:
`631`: the TCP port for CUPS must be exposed

## Create and run container with:

`docker run -dit --restart unless-stopped --name cups-airprint -e CUPSADMIN=admin -e CUPSPASSWORD=pass -v ~/cups-data/config:/config -v ~/cups-data/services:/services -p 631:631 idumzaes/cups_airprint`

### CUPS Web Config
CUPS will be configurable at http://[diskstation]:631 using the CUPSADMIN/CUPSPASSWORD when you do something administrative.
