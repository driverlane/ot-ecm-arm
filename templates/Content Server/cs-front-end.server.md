# cs-front-end.server

This template creates Content Server front end servers. The number of servers is determined in the `cs-instance` template.

Content Server front end servers require at least one Content Server admin server for a functioning Content Server instance.

## parameters

* *servername* - the name of the server, for multiple servers an number will be appended to the name
* *adminUsername* - the admin user for the machine
* *adminPassword* - the password for the admin user, this will need to be specified in the deploy command and should not be added to any parameters files.
* *serverImageUrl* - the location of the base VM image for copying.