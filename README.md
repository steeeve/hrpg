# HRPG

Another command line interface for HabitRPG: Your Life the Role Playing Game.

Mostly intended to play nice with other unixy programs i.e.

```sh
$ hrpg stats | grep HP
# HP 47
# MAX_HP 50

$ hrpg todos
# Feed the fish
# Sort mail

$ echo "Remember the milk" | hrpg todos
# Remember the milk
# Feed the fish
# Sort mail
```

## Installation

Install it with:

    $ gem install hrpg

## Usage

To use you need to set up a config file with your settings:

```yaml
# in ~/.hrpg
user_id: YOUR_HABITRPG_USER_ID
api_token: YOUR_HABITRPG_API_TOKEN
```

### Commands

Once your config is set up the following commands should work.

Show your current status (pretty formatted):
```sh
$ hrpg status
```

![hrpg status screenshot](https://dl.dropboxusercontent.com/u/443279/hrpg_status.png)

Show your full stats:
```sh
$ hrpg stats
# HP 47.1
# MAX_HP 50
# MP 44
# MAX_MP 44
# EXP 117
# TO_NEXT_LEVEL 220
# PER 0
# INT 0
# CON 0
# STR 0
# LVL 7
# GP 11.48107934389596
```

List your habits:
```sh
$ hrpg habits
# Study
# Turn out the lights
```

List your dailies:
```sh
$ hrpg dailies
# Feed the fish
# Sort mail

$ hrpg dailies --completed
# Feed the fish

$ hrpg dailies --uncompleted
# Sort mail
```

List your todos:
```sh
$ hrpg todos
# Remember the milk
# Put the bins out

$ hrpg todos --completed
# Remember the milk

$ hrpg todos --uncompleted
# Put the bins out
```

Add tasks by using STDIN:
```sh
echo "Remember the milk" | hrpg todos
```

For more information:
```sh
$ hrpg help
```
