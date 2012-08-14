#Scanbot

Work in progress Cortana bot for doing nmap scans. Not currently intended for use, but knock yourselves out. This bot is intended to assist with scanning in engagements with many target ranges that should be scanned seperately. Less time scanning, more time in the shell.

Intended to function similar to an IRC bot, taking commands from the team in the Event log.

Currently semi-functional. Performs db_nmap with parameters defined in the "scanbot.conf" config file.

db_nmap -p 3389,80 $targets

To communicate with the bot preface commands with "!bot".  Current testing commands are:

help : displays the current command set with a brief description.
scan $Target : adds an address to the bottom of the scan queue.
filequeue "/path/to/file" : import from a file on the server hosing scanbots local drive.
showqueue : display the current scan queue.
drop $Target : drops the $Target from the queue
clearqueue : clears the entire queue.

Bot will read initial values from a supplied file defined in the "scanbot.conf" file. Addresses in this file should be one per line.
To help keep the bot from talking to itself, please define the Bots username in the "scanbot.conf" file.

-Zinterax
