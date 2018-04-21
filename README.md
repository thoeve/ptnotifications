
# PT Notifications
<img src="https://i.imgur.com/6q1wcy0.png" width="200">

A official ProfitTrailer addon.  
The solution to tracking your daily ProfitTrailer profit on the go.

## Features and commands

[PT Notifications video](https://www.youtube.com/watch?v=IAkIHYvsrAo)


#### Features
- PT Notifications has support for both Discord and Telegram.
- Runs on Windows, Linux and macOS.
- Sends detailed buy and sell notifications. Including DCA, profit in dollars and more
- Sends update notifications when there is a new ProfitTrailer release.
- Sends Sell Only Mode notifications
- Sends notifications when ProfitTrailer runs into a error.

#### Commands
- [/update] Sends list of options
	- [/today] List of today's statistics including profit, balance and more.
	- [/yesterday] List of yesterday's statistics including profit, balance and more.
	- [/dca] List of DCA
	- [/pairs] List of pairs
	- [/last] Last 5 sales
	- [/all] Contents of /dca, /today and /pairs

- [/settings] Sends list of options
	- [/enable_som] Enables Sell Only Mode
	- [/disable_som] Disable Sell Only mode
	- [/blacklist] Adds given coin to _trading_enabled = false
	- [/whitelist] Adds given coin to enabled_pairs = list

- [/version] Sends version numbers of running instances and whether there is a update available.
- [/alive] Responds when PT Notifications is up and running.
- [/help] List of available commands.


## Getting Started

These instructions will get you a copy of the project up and running on your local machine or server.

### Prerequisites

What things you need to install the software and how to install them

If you already have ProfitTrailer running on the same machine you can ignore this.

Make sure you have Java 8 (1.8.0_131 and up) installed on your computer. (Java 9 will not work).  
Windows & Linux require Java 8 JRE - [Download](https://www.java.com/en/download/).  
Mac OSX requires Java 8 JDK - [Download](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.htm).  

### License

To run PT Notifications you need to have a valid ProfitTrailer PRO license.

### Creating bots
#### Telegram
-	In Telegram, send a private message to @BotFather (NOT to be confused with TheBotFather ​channel)
-	Once there type “/​newbot” ​to create a bot. Answer the questions ​by typing answers and pressing enter.
You will receive a message ​containing your bot token.
-	Start a chat with your bot's name (for example ​@MyTPBot) and press start button ​
-	Start another ​chat with [https://t.me/MyTelegramID_bot.]([https://t.me/MyTelegramID_bot)
-	If that doesn't work, try a chat with [https://​telegram.me/​id_chatbot.](https://​telegram.me/​id_chatbot)
or paste @id_chatbot into a telegram chat and click it. It should open the chat id bot in a new chat.
or send a message to: @userinfobot with content: /start
-	Finally, here is a link to a page [https://ebotstore.de/bot/mytelegramidbot-telegram](https://ebotstore.de/bot/mytelegramidbot-telegram) with a couple more ID chatbots for telegram that you can click if the above doesn't get a valid response.

#### Discord
- In Discord, create your own server by clicking the + button in the server menu on the left. Discord published their own guide [HERE!](https://github.com/reactiflux/discord-irc/wiki/Creating-a-discord-bot-&-getting-a-token)
- Create a text channel by right clicking on your server icon and selecting “Create Channel”.
-	Create a discord bot. There is a great guide HERE!
-	Add the bot to your server

### Installing

Download the latest version from the releases page.

#### Quick notes to success
- to get the "discord_channel_id =" please go to Discord settings > appearence > developer mode on then right click on the channel you want the bot in and click Copy ID - this will be a number please use this and not the channel name or it will say bot token error

###### Prepare your ProfitTrailer instances
- Give every ProfitTrailer instance you run a unique ```server.sitename``` in the ```application.properties``` file. This is so it's easier to recognize your bots easier when receiving notifications.
- Read note above Make sure to set the ```server.api_token``` variable in the ```application.properties``` file for each instance as well. This value can be any random arrangement of characters. This is needed so the addon can request access to the trade data. 
- MAKE SURE TO RESTART PT AFTER EDITING PT BEFORE STARTING!


###### Update the PT Notifications settings
```
#Amount of PT instances you have running
profitTrailer_instances = 1

profitTrailer_address_1 = 
profitTrailer_license_key_1 = 
#Make sure it matches the server.api_token variable in application.properties of your PT instance
profitTrailer_instance_api_token_1 = 

#Example
#profitTrailer_address_2 = http://localhost:8082
#profitTrailer_license_key_2 = 1234567abcd8910
#profitTrailer_instance_api_token_2 = bot_api_token

#Enable or disable Telegram notifications
telegram_enabled = true/false
telegram_bot_token = 
telegram_channel_id = 

#Enable or disable Discord notifications
discord_enabled = true/false
discord_bot_token = 
discord_channel_id = 

#Enable or disable Sell Only Mode notifications
som_notifications = true
#Enable or disable ProfitTrailer error notifications
error_notifications = true
#Enable or disable update notifications
update_notifications = true
#Add error messages that need to be ignored seperated by a comma i.e. SomeKindOfExchangeError,AnotherExchangeError
error_filter = BinanceWebSocketAdapterKline,APIKEY_INVALID
```

###### Getting PT Notifications to run

Windows
```
Simply run the Start_windows.cmd file in the zip.
```
macOS & Linux
```
Simply run the Start_linux.sh file in the zip.
Or
Open terminal > navigate to the folder containing the .jar.

Run the jar using:
java -jar PTNotifications.jar -XX:+UseG1GC -XX:+UseStringDeduplication -XX:StringDeduplicationAgeThreshold=1 -Xmx128m
```
