# 1. Implement Auto-renew SSL:
```sh
I used this command: `sudo certbot renew --dry-run`  & used crone job for it  `* * */15 * * root certbot -q renew --apache >/dev/null 2>&1`
Manual way:   `sudo certbot certonly --force-renew -d freelyy.hopto.org -d freelyy.hopto.org`
```
# 2. Diff b/w certonly and renew in certbot:
 ```sh
The certonly generates the certificate per run per certificate. but renew can renew many certificates in one run. The other difference is certonly provides a user interaction facility via commands.
```
# 3. Try to implement a proxy pass:
# 4. Study On Directory Block:
```sh
The <virtualHost> contains directives referring to one host.
`<VirtualHost *80>`
`ServerAdmin doamin.com`
`DocumentRoot /usr/www/site.virtual/` 
`ServerName www.butterthlies.com` 
`</VirtualHost>`

**File and Location Options**

If you need further control over specific files within a directory on your server, use the <Files> directive. This directive controls the behavior of the web server with regard to a single file. The <Files> directives will apply to any file with the specified name.

**Override Options with htaccess** 

In addition to the configuration methods discussed above, by default Apache will read configuration options for a directory from a file located in that directory. This file is typically called .htaccess.

**Location Options**




