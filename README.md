![index.svg](2025/themes/pubsub/components/site-header/images/fldc25-logo/index.svg)

# FLDC Archives

Using:

```
httrack https://www.fldrupal.camp -O . -N "%h%p/%n/index%[page].%t" -WqQ%v --robots=0
```

Deploying to server:

```
git clone --no-checkout https://github.com/JCL324/fldc-archives.git .
git sparse-checkout init --cone
git sparse-checkout set [year] e.g. 2026
git checkout main
```

Configure Apache files, and `sudo a2ensite [year].fldrupal.camp`

Finally, `sudo certbot -v`, select the site #.

Hosted by CND on Linode.
