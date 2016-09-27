# Dehydrated-docker
## A small Docker image base on Alpine for automate certs generation. 

https://github.com/lukas2511/dehydrated

`docker pull valentinnc/dehydrated`

Example :

`docker run --rm -v /tmp/domains.txt:/dehydrated/domains.txt \`

`-v /var/www/acme-challenge:/var/www/dehydrated \`

`-v /etc/certs:/dehydrated/certs \`

`valentinnc/dehydrated -c`

This example use 3 volumes :

- **/var/www/acme-challenge** is the folder for ACME challenge
- **/tmp/domains.txt** is your domains list
- **/etc/certs** where you get your certs

You can override the **domains.txt** file using `-d example.com` flag to specify your domain. 

You can override the default configuration using a volume : `-v /path/to/config:/dehydrated/config` and a flag `-f /dehydrated/config`
