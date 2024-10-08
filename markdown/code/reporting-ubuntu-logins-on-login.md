## Reporting Ubuntu logins on login

When setting up an Ubuntu server, I would recommend sensing if logins are being attempted by outside sources.

Even if you aren't storing data that needs to be secure, it could be valuable to know if logins against your system are successful.

Given the [Ubuntu tutorial to view log files](https://ubuntu.com/tutorials/viewing-and-monitoring-log-files#2-log-files-locations), a fairly simple auth log could be transmitted on login from `/var/log/auth.log`.

A simple enough way to show the last 10 actions done on the server (including 3 actions that are done on the current login), you can add to .bashrc:

```
echo "Last 10 auth actions:

"
tail /var/log/auth.log
```
