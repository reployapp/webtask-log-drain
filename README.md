# Webtask log drain

Use this setup on Heroku (or other service) to stream your webtask logs to Papertail (or other service). This is needed until webtask.io lets you stream logs/errors another way.

## Heroku setup

Get setup on Heroku. Get setup on Papertrail. Clone this repo.

```
% heroku create yourapp-logs
% heroku drains:add syslog+tls://<host>.papertrailapp.com:<port> --app yourapp-logs
% heroku config:set WEBTASK_TOKEN yourToken
% heroku config:set WEBTASK_CONTAINER yourContainer
% git push heroku master
