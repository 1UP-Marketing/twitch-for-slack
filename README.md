## Features
- Detect if a Twitch stream is online
- Send notification to a Slack webhook if a stream comes online
- Can watch multiple streams to come online

## Installation
- Simply clone this repo.
- Copy config.json.example to `config.json` like `cp config.json.example config.json`
- Run `npm install` command.
- Install a [incoming-webhooks](https://api.slack.com/incoming-webhooks) on your Slack.
- Add your link for the Slack incoming-webhooks in the `config.json` file.
- Setup crontab to run the script every min or so. with something like this '* * * * * node /home/twitch/twitch-to-slack/index.js >/dev/null 2>&1'

## Configuration
- `clientToken` : Application's client_id, requested by Twich API. You have to register https://www.twitch.tv/kraken/oauth2/clients/new your application to get it.
- `chaineID` : Name of the stream to monitor example : ["crazyonerob", "bacon_donut"]
- `slackHookUrl` :  Link to your Slack incoming-webhooks.
- `slackHookName` :  Name to display when you will get notified on Slack.