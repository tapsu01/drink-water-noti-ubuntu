# Keep back straight and drink water remind by Ubuntu 20.04 notification

1. Create a job which runs every 15 minutes

```sh
crontab -e
```

2. Add this line to `crontab` config

```sh 
*/15 * * * *  XDG_RUNTIME_DIR=/run/user/$(id -u) notify-send "Hey Tu" "Keep your back straight and drink water!"
```

3. Restart cron daemon

```sh
/etc/init.d/cron restart
```

4. Enjoy!
