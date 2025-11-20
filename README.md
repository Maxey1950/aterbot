# AterBot ✨
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](/LICENSE)
### Keep your Aternos server alive 24/7.
Please star this project <3
<br/>

# Important Notice 📢
### This project will be unmaintained until at least 2024.<br/>But you can use it as usual.

# Requirements 🎒
1. A Render account.
   Sign up at: https://render.com/

2. An UptimeRobot account.
   Sign up at: https://uptimerobot.com/signUp

3. A Minecraft server you owned.
   Make sure your server settings `online-mode` set to `false`!
   And you should have an OP permission!

# Setup on Render ⚙
1. **Fork this repository.**
   Click the "Fork" button at the top right of this page.

2. **Create a new Web Service on Render.**
   - Go to your Render Dashboard.
   - Click "New +" and select "Web Service".
   - Connect your GitHub account and select your forked repository.
   - Render will automatically detect the `render.yaml` file and configure the service.

3. **Configure Environment Variables.**
   - In your Render service dashboard, go to the "Environment" tab.
   - Add the following environment variables:
     - `MC_HOST`: Your Minecraft server address.
     - `MC_PORT`: Your Minecraft server port.
     - `MC_USERNAME`: The username for your bot.

4. **Deploy the service.**
   - Click "Create Web Service". Render will build and deploy your bot.

5. **Set up UptimeRobot.**
   - Once your service is deployed, copy the URL from your Render dashboard.
   - Go to your UptimeRobot dashboard.
   - Click "Add New Monitor", select "Monitor Type" to "HTTP(s)".
   - Paste the URL from Render into the "URL (or IP)" field.
   - Click "Create Monitor" twice.

Finally... DONE! Enjoy your free 24/7 Aternos server.

# FAQ ❓
> #### Q1: How to fix `unsupported/unknown protocol version: ###, update minecraft-data`?
<details><summary>A1:</summary>

This project is using the `mineflayer` module.
**It may not supported on your server version yet.**
I'm trying to periodically check for updates, so please be patient.
</details>

<hr/>

> #### Q2: How to fix `Invalid move player packet received`?
<details><summary>A2:</summary>

It seems your bot escaped from the bedrock room.
So you have to wipe the playerdata in your server.
1. Go to the management page of your Aternos server.
2. Click `Files` in the left section.
3. Delete the `world/playerdata/<UUID>.dat`, `<UUID>.dat_old` file. (the UUID is your bot's UUID)
4. Restart the bot.

**Lock the bot somewhere as soon as possible!**
**And change the bot's gamemode to `Creative` to not die.**
</details>

<hr/>

> #### Q3: My bot leaves permanently after n hours.
<details><summary>A3:</summary>

Aternos automatically bans AFK players from your server.
So just unban your bot, if it's banned.
</details>

# CAUTION ⚠
### Aternos might detect your suspicious actions and delete your account!
**By using this, you acknowledge that you're responsible for any problems arise.**
