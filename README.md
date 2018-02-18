# PT Notifications

The solutions to tracking your daily Profit Trailer profit.
Website: [ptnotifications.com](https://ptnotifications.com)

![N|Solid](https://ptnotifications.com/img/feature-mobile.png)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine or server.

### Prerequisites

What things you need to install the software and how to install them

If you already have Profit Trailer running on the same machine you can ignore this.
Make sure you have Java 8 (1.8.0_131 and up) installed on your computer. (Java 9 will not work)
Windows & Linux require Java 8 JRE - [Download](https://www.java.com/en/download/)
Mac OSX requires Java 8 JDK - [Download](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.htm)

### License

Get your license on [ptnotifications.com](https://ptnotifications.com)

### Installing

Download the latest version from the releases page

Update the PT Notifications settings:
```
License_key = YOUR LICENSE KEY

ProfitTrailer_Address = YOUR PROFIT TRAILER ADDRESS e.g 172.456.231.12:8081
ProfitTrailer_Password = YOUR PROFIT TRAILER PASSWORD
timeZoneOffset = +1

Telegram_enabled = TRUE/FALSE
Telegram_bot_token = YOUR TELEGRAM BOT TOKEN
Telegram_channel_id = YOUR TELEGRAM CHAT ID

Discord_enabled = TRUE/FALSE
Discord_bot_token = YOUR DISCORD BOT TOKEN
Discord_channel_id = YOUR DISCORD CHANNEL ID

som_notifications = TRUE/FALSE
```

###### Getting PT Notifications to run

Windows
```
Simply run the Start.cmd file in the zip.
```
macOS & Linux
```
Open terminal > navigate to the folder containing the .jar.

Run the jar using:
java -jar ptnotifications.jar -XX:+UseG1GC -XX:+UseStringDeduplication -XX:StringDeduplicationAgeThreshold=1
```

## Support
Join our Discord or Telegram for support:
[Telegram](https://t.me/ptnotifications)
[Discord](https://discord.gg/6KEz6aN)

