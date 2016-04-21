# Webtask log drain

Use this setup on Heroku (or other service) to stream your webtask logs to Papertail (or other service). This is needed until webtask.io lets you stream logs/errors another way.

## Heroku setup

Get setup on Heroku. Clone this repo.

```
% heroku create yourapp-logs
% heroku drains:add syslog+tls://<host>.papertrailapp.com:<port> --app yourapp-logs
% git push heroku master
