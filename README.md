IP: 197.45.254.32

SSH port: 2200

URL: www.197.45.254.32.xip.io


Summary and steps:

1- I have a static ip , so i decided to make a dedicated server better than taking a vps for trial period.

2- Installed oracle VM , and installed ubuntu server 18.04 LTS.

3- While installing i enter the static ip and the default gateway and subnet mask.

4- Specify the username with sudo privileges, because root is disabled by default.
5- Run "sudo apt-get update" and then "sudo apt-get upgrade".
6- Add user for reviewer called grader, and give him sudo access in the file etc/sudoers.
7- Generate key pair for the admin and the grader, and put the .pub file in the .ssl folder in the admin folder and samfe for grader folder.
8- Force key pair authentication and disable login via SSH password.
9- Allow ports (ssh,80,2200,123).
10- Install apache2 "sudo apt-get install apache2".
11- Install mod_wsgi "sudo apt-get install libapache2-mod-wsgi".
12- Configure the apache to work with wsgi when the ip is called with "/" to route for the directory of the web application (Wsgialias,etc...).
13- I followed steps for deploying a flask application on ubuntu "https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps".
14- Installed the programs and packages i need (git,python,pipm,flask,packaging,oauth2client,redis,passlib,flask-httpauth,sqlalchemy,flask-sqlalchemy,psycopg2-binary,bleach,requests).
15- Fixed some errors that appears in the item catalog project that appeared when deployed the application on the internet, like file permissions and file paths.
16- Make git project and commit the initial commit in the web application folder.
17- Create empty repository in github.
18- Connect the local repository to the remote repository on github.
19- Fixed error in google OAuth2 because i must have a TLD (Top-Level-Domain), so i used xip.io free DNS service.
20- Put the url of the site in the Auth javascript origin redirects, and it will accept the url, as i tried to put the IP and it give me error.
21- Facebook login is hard to do because it want my site to be HTTPS.
22- Configure the local timezone to UTC.

grader key:

-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEA5tTVhweN2hKyrc2vySefVuTA6BzXoxMY6woVnypOBadQdyKB
DlcI5m7U944GMSLherKOmX8f4NFAz8iG1XmXqUagSs8IETjzObQ5HnLXsbyCi9Ds
cPqz6JVUXycQyWWTeY8twZzTr8UEGGVj4uqqd2RMGiP5kvGn7IR3UWobC12wSbxU
jxAxVVTaqaBalhcZxULbqmMH3wEjIPqzaruuNP4LCJsm2W60PBKrzyPkt0c6Hmtk
sr9cKLPfgKbj5chY6n2C23ewgBoJSiqjio6tiRCXg+OlK5LJjX5MILt32b5dMZWk
4stYY3bbCxVDiWFdY/0WwFd6AN5nyGW0Z7AJqwIDAQABAoIBAE5g5GQmJ39tq+gi
GFc4Mf2CTRJDgODpgiOE2BSke7ultUfOmn2xBd+gsIWiXu3eRyuvZ4YtSTjANL6Y
+1ePIvUiexkLtVSLvuLQFDkHi7/ZH4a0GSS/q8kEs5JfpG6OJAY5nLLKOoLLZfmW
q9UIE3vYvZJ+tqazkW5ZCF7HpYk00InZoxl1kJLs/0MsP3xIqIvOvTaUQFugG0/K
4biU2XtIjbe+ou34lVDv+gwqSTJCsJN8MCiNg8EGJRC8IpnBDtMESCb3O4wA6kQL
d9kqfeKfAyTQD4ORlrNZue1kX2G2AD1BbTgGcCFlEcCAZ65xUFtKl6czwOt4jq/T
WQqw1KkCgYEA/NfjzVkt014neryQkHkgJjTaGCpvcbTfo533JcPYRsfs14ZIMVl2
GpIhjCCPFRizW+4SJ/n5S2zclaKNFhtbMuilDnSVli4z40XjOkLgptknAjW8S/Ng
Ujc3imF9xADRtXutSQdsTNKjXHIseomoaG9gn9hgJmJmKAdpb7XPqrcCgYEA6baX
k6gijzKCNwzUfW6zC3y49VH8x3Aa0KDLsfcE4U9i5D4cxF7bQvaUIAORyvQ6CNgL
y8E7oiaE8/HxaMNmu+p036Dh3ejK5GvFyN8amdWZ1vj2t5GSMDsoCatKHjaHU+9c
4Mf9qVWcx4ytvoJLL/bju5lpY1euAXdnru83tK0CgYB6C3OIIW2/QwlnczGMqwrb
plNHquQUTKxOe+daMUhqEgK+nbCnMXmSpcrPqr+l/UBGNYpKBZ1RzQBEsivL6fSB
hE53xcqWrUKah5eA/dsWbmcn5+w19QofZUvH3fso6wROx54DTDP4eQwliW7yzxOd
JXXMclMm9AQ/eiRoqafNzQKBgHLQpP6BJxk6MwZgYzOL4qHOD/9U294OkN3VYLx5
IgieO3LtoKxH/WeUQ4jGuCUAflJB8OmUcHtkeQRu464X8Kx4rhn+q3edGa/F0lCw
ah0Q9pbJkEr2VN8k8LJvV+Yn26u8d+Bl35QE3xSZY/GniNBzdcV/xGptdKp7wpAK
LU+xAoGBALDCSIuPO4KydUG8h9eM2W9nmFppvrJfbcOq6PP1oWPbGhVg5wfkrDST
qR/IoVcKGMpPkRMWN0uS7Clp5qWkkSBuhMh2LsdLyQUAcOah6eWBIhUBEgqAGakS
STiklAima+/luUimPGH0098BZmBi1UruBXGB6toHqfmP/xH7R1Nn
-----END RSA PRIVATE KEY-----
