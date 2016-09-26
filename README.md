# Dehydrated-docker
## A small Docker image base on Alpine for automate certs generation. 

Example :

`docker run -v /tmp/domains.txt:/dehydrated/domains.txt \`
`-v /var/www/acme-challenge:/var/www/dehydrated \`
`-v /etc/certs:/dehydrated/certs \`
`valentinnc/dehydrated -c`

This example use 3 volumes :

- **/var/www/acme-challenge** is the folder for ACME challenge
- **/tmp/domains.txt** is your domains list
- **/etc/certs** where you get your certs
