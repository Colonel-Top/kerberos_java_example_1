# kerberos_java_example_1
This is just a small project, copied from somewhere on the net, with an example code of a client and a server using Kerberos

In order for it to work you will need:

1) 2 principals defined in your kerberos realm:
webclient@YOUR.REALM
webserver/<hostname>@YOUR.REALM

These names are configurable in client.properties and server.properties

2) credentials for these users stored within a file called ./creds.keytab (addressed by jaas.conf file)
example:

ktutil
ktutil:  addent -password -p webclient@YOUR.REALM -k 1 -e aes256-cts-hmac-sha1-96
Password for webclient@YOUR.REALM: 
ktutil:  wkt ./creds.keytab
ktutil:  exit

Hard coded:
the files ./server.properties, ./client.properties and ./jaas.conf are hard coded in the application (for now)


