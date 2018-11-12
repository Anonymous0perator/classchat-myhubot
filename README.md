# classchat-myhubot
ClasChat Hubot Adapter

This is a WIP and will probably be unreliable for a while, so use at your own risk

Overview

We're going to install a new stock hubot, and install this hubot "adapter" so it can talk to ClassChat.

1. Install a hubot

Create a new hubot. There are several ways to do this but the simplest might be using this hubot command:

hubot --create myhubot
You might also like to use the yeoman hubot installer. Check out the hubot docs for help getting a hubot running.

2. Install the Adapter

Once your hubot is working, change directory into your new bot code:

cd myhubot

Then install the adapter with npm:

npm install hubot-classchat-myhubot --save

3. Optional environment variables

Set the following environment variables:

HUBOT_LCB_ROOMS You can see these IDs in the URL for the room. NOTE: this is a comma-separated list.
HUBOT_LCB_TOKEN can be found in the Let's Chat interface. Click on your username and look under "Auth Tokens."
Set these two environment variables with export:

export HUBOT_LCB_TOKEN=NTRiNjg5NmYyMDZiMzEwMDAwYTAxNmZiOjE0ZTg2ODMwYz...
export HUBOT_LCB_ROOMS=5279facb1015642226000011,5394ffbabdea44e815000003
Additionally, three more environment variables are optional and have default values:

export HUBOT_LCB_PROTOCOL=http
export HUBOT_LCB_HOSTNAME=localhost
export HUBOT_LCB_PORT=5000
4. Create a new user in Classchat

In the Classchat web interface, create a user with the same @name as your bot, like @myhubot.

You can customize it when you boot the hutbot, like ./bin/hubot --adapter lets-chat --name myfancyname.

Tip for Gmail users: classchat 0.3 uses gravatar for avatars. So if you want to customize the bot avatar, you could use a Gmail alias like myemail+hubot@gmail.com, then customize that avatar in Gravatar.

5. Let's go! Start the server.

To get the hubot running, start the server with the lets-chat adapter.

bin/hubot -a classchat-myhubot
If everything goes well, your bot will join you in your classchat instance.
