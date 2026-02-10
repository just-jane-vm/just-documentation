# overview 
all commands must be prefixed either with `!` or the word `bang`.
commands listed here have will attempt to send a response when the --help flag is used, e.g. `bang my-color --help`
in the documentation below a missing example section implies the command is self evident, and a missing alias section implies the command has no aliases.

when a user display name is required for an argument their aare a few acceptable variations generally:

- including the `@` symbol is optional, this can be useful in twitch chat to enable auto-completion of a user name
- a username has two versions the login name (all lower case) and the display name (set by the user where case is custom), either option is okay

## static commands

### ping
test command, simply responds with pong.

### github
get link to the github website.

### discord
get invite link to discord server.

### raid
print the standard raid messages.

### seiso
so sei we all.

### bahms
who are we?

### toerig
erm...

#### alias
throne

### barknote
xD

## user commands

### my-color
gets your "color" within the stream system.
everyone is assigned an initially random color that is used for various things.
all colors are unique within the system.

#### example
```
[user]: !my-color
[just__streamerbot]: @user your color is #deadff
```

### set-color
attempts to set your color.
if someone already has your color the command fails silently.

### giga-vip
gets current giga-vip level for users.
with certain admin scopes this command is also used to add/remove levels.
option to provide a user aas an argument exists, if a user is not provided as aan argument the command assumes the chatters user is desired.

#### alias
gvip

#### examples
```
[user]: bang giga-vip
[just__streamerbot]: @user is a level 69.420 giga-vip!
[user]: !giga-vip @other_user
[just__streamerbot]: @other-user is a level 420.069 giga-vip!
```

### gifta-vip
transfers some of the callers giga-vip levels to another user.
this command fails if the calling user does not have enough vip levels to cover the transaction.
requires both a target user followed by an amount (number).
this command should only generate a just__streambot response if it fails, it is suggested that users using this command check that it works using the giga-vip command before and after a transfer.

#### examples
```
[user] !gifta-vip @other_user 0.67
```

### choice
get a random choice from a comma separated list.

#### alias
choose

#### examples
```
[user]: !choice one, two, three
[just__streambot]: given these options...i choose one!
```

## titles
some commands and sounds are unlocked by spending giga-vip.
the table below enumerates the available titles, their cost, and what they do.
titles can be purchased only once.

|title|cost|description|
|-:|:-:|:-|
|rain-maker|25|20 seconds of rain sounds, cana be stacked|
|thunder-god|50|a thunder crack, available while rain is active|
|silver-slurper|50|someone slurping|
|ara-ara-mommy|50|someone saying ara ara|
|uwu-people|50|someone saying uwu|
|ermily|50|someone saying erm|
|dominatrix|100|whip sound|
|doggirl-trainer|250|click click|

#### examples
```
[user]: !uwu-people
[just__streambot]: you already have this...
[user]: !ara-ara-mommy
```
### my-titles
prints the list of titles a user currently has

## moderator only commands
commands that can only be used by users with access.
users without the correct access who attempt to use these commands will be timed out.

### start-announcing
starts the announcements, this should almost always be invoked by jane using the start-stream alias.

#### alias
start-stream

### stop-announcing
stops the announcements, generally just use the end-stream alias HOWEVER note that end-stream is overloaded in other systems using stop-announcing _only_ stops the announcements without trigging any other system.

#### alias
end-stream

### run-ad
runs ads for a parameterized number of seconds.
should be invoked with an increment of 30 with a max value of 180

#### alias
ad
