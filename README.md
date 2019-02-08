# Snips Kaamelott action
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/agileek/snips-skill-kaamelott/master/LICENSE.txt)

This is a Snips kaamelott action written in Python and is compatible with `snips-skill-server`.
This action parses the kaamelott intents. The result is then played through wav.

## Setup
### Prerequisites

You'll need to add the Kaamelott french skill in your assistant. It's available on [Snips' console](https://console.snips.ai)

### SAM (preferred)
To install the action on your device, you can use [Sam](https://snips.gitbook.io/getting-started/installation)

`sam install action -g https://github.com/agileek/snips-skill-kaamelott.git`

### Manually

Copy it manually to the device to the folder `/var/lib/snips/skills/`
You'll need `snips-skill-server` installed on the pi

`sudo apt-get install snips-skill-server`

Stop snips-skill-server & generate the virtual environment
```
sudo systemctl stop snips-skill-server
cd /var/lib/snips/skills/snips-skill-kaamelott/
sh setup.sh
sudo systemctl start snips-skill-server
```

## How to trigger

`Hey Snips`

`Balance du kaamelott`

Look into `trainings_and_slots/random_kaamelott_intent` to see which phrases are recognized, feel free to add your own

## Logs
Show snips-skill-server logs with sam:

`sam service log snips-skill-server`

Or on the device:

`journalctl -f -u snips-skill-server`

Check general platform logs:

`sam watch`

Or on the device:

`snips-watch`
