# Watford AI Discord Bot

## Features

* `/chat [message]` Chat with Watford AI!
* `/private` Watford AI switch to private mode
* `/public`  Watford AI switch to public  mode
* `/replyall`  Watford AI switch between replyall mode and default mode
* `/reset` Clear Watford AI conversation history

### Chat


### Mode

* `public mode (default)`  the bot directly reply on the channel

 

* `private mode` the bot's reply can only be seen by the person who used the command



* `replyall mode` the bot will reply to all messages in the server without using slash commands

   > **Warning**
   > The bot will easily be triggered in `replyall` mode, which could cause program failures

# Setup

## Install

1. `pip install -r requirements.txt`
2. **Rename the file `.env.dev` to `.env`**

## Step 1: Create a Discord bot

1. Go to https://discord.com/developers/applications create an application
2. Build a Discord bot under the application
3. Get the token from bot setting

  
4. Store the token to `.env` under the `DISCORD_BOT_TOKEN`

  
5. Turn MESSAGE CONTENT INTENT `ON`

  
   
6. Invite your bot to your server via OAuth2 URL Generator

 

## Step 2: Generate a OpenAI API key

1. Go to https://beta.openai.com/account/api-keys

2. Click Create new secret key

  

2. Store the SECRET KEY to `.env` under the `OPENAI_KEY`

## Step 3: Run the bot on the desktop
1. Open a terminal or command prompt
2. Navigate to the directory where you installed the Watford AI Discord bot
3. Run `python3 main.py` to start the bot

## Step 3: Run the bot with Docker

1. Build the Docker image & Run the Docker container `docker compose up -d`
2. Inspect whether the bot works well `docker logs -t Watford AI-discord-bot`

   ### Stop the bot:

   * `docker ps` to see the list of running services
   * `docker stop <BOT CONTAINER ID>` to stop the running bot

### Have a good chat!

## Optional: Setup starting prompt

* A starting prompt would be invoked when the bot is first started or reset
* You can set it up by modifying the content in `starting-prompt.txt`
* All the text in the file will be fired as a prompt to the bot  
* Get the first message from Watford AI in your discord channel!

   1. Right-click the channel you want to recieve the message, `Copy  ID`
   
      
    
   2. paste it into `.env` under `DISCORD_CHANNEL_ID`
