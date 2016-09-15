# Hipchat Bot for posting Funny Stuff on specific Jira Issue Number

# Dependencies

You need your own Hipchat instance.
The [JIRA Integration for HipChat by Atlassian](https://marketplace.atlassian.com/plugins/com.atlassian.labs.hipchat.hipchat-for-jira-plugin/cloud/overview)

# Installation

The Bot is easy to setup on an NodeJS Hoster like [Heroku](https://heroku.com).

Before uploading edit the config.json file in the root directory. Change `issue_numbers` to your personal preference and `localBaseUrl` to your Heroku Url. In the admin interface of your heroku app add the Plugin Heroku Redis. Its completely free if you select the "Hobby Dev" preset.

Now upload the App to Heroku.

Check if the "REDIS_URL" environment variables is set. You can check that if you have installed the [Heroku Cli](https://devcenter.heroku.com/articles/heroku-command-line). If its installed on your local machine and if you're logged in type
```bash
heroku config
```
and you should see the REDIS_URL. If your don't see it check if the Heroku Redis Plugin is active.
After that set NODE_ENV to production
```bash
heroku config:set NODE_ENV=production
```
After that just add the Plugin with the Url to your Hipchat instance.
