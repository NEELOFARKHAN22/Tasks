# 1. Implement Auto-renew SSL:
```sh
*I used this command: `sudo certbot renew --dry-run`  & used crone job for it  `* * */15 * * root certbot -q renew --apache >/dev/null 2>&1`
Manual way:   `sudo certbot certonly --force-renew -d freelyy.hopto.org -d freelyy.hopto.org`

