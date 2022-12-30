# SlackNotifyLogger

### Create Slack bot
1. Create a Slack account for the bot if you don't already have one.
2. Go to the Slack API website (https://api.slack.com/) and click on the "Start Building" button.
3. Select the "Create a new app" option.
4. Give your app a name and select the workspace where you want to develop it.
5. Click on the "Create App" button.
6. From the "Add features and functionality" section, click on the "Bots" option.
7. Click on the "Add a Bot User" button.
8. Give your bot a display name and default username, and then click on the "Add Bot User" button.
9. Take note of the "SLACK_OAUTH_TOKEN" values, as you will need these later.
10. Click on the "Install App" button, and then click on the "Install App to Workspace" button to install the app to your workspace.

### How to use this dependency?
- `dotnet add package SlackNotifyLogger`
- setup NotifyLogger in Program.cs file
  ```
  Host.CreateDefaultBuilder(args)
      .ConfigureWebHostDefaults(webBuilder =>
      {
          webBuilder.UseStartup<Startup>();
      }).SlackNotify();
  ```
- add config in appsetting.json file
  ```
    "SlackNotify": {
      "channel": "your channel for notify message",
      "serviceName": "your service name",
      "token": "your token"
    }
  ```
