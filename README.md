# Creating certificates with Let's Encrypt

## Reference
https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/

## Requirements
- nginx
- certbot

### Summary
ex. domain <mywebsite.com> (Note you need to have a custom domain to create the certificates)
``` 
sudo nginx -t && sudo nginx -s reload
sudo certbot --nginx -d mywebsite.com -d www.mywebsite.com
```

### Possible Errors
If error message about cannot find PID 
```
sudo service nginx stop
sudo /etc/init.d/nginx start
```
