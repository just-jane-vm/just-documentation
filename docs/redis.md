# redis cache usage
ref cache client repository for client code

## APIs

### user/{id}

#### scopes
a set of strings that represent different scopes a user has access to in an rbac like conceptual system.
currently this is just used as a placeholder for something eventually more robust.
used to implement restricted chat commands and sounds.
current scopes are:

|scope|description|
|-:|:-|
|thunder-god|grants access to the thunder sound|
|ara-ara-mommy|grants access to the ara ara sound|
|uwu-people|grants access to the uwu sound|
|silver-slurper|grants access to the slurp sound|
|ermily|grants access to the slurp sound|
|alerts|access to the !alert whisper system|
|marketing|access to the !start/stop-announcing commands|

#### shame-token
an integer number of "shame tokens" granting access to the !jane command

#### tts-bank (removing)
a double containing some amount of giga-vip that has been reserved for use in the tts system.
need to remove this, refund levels, and start just using mega-vip

#### tts-voice
a string identifier for the custom tts voice the user has configured as their default

### jill

#### memory/{user_id}/name
#### memory/{user_id}/something
#### memory/internal/transition-counter
the number of transitions jill has executed

#### memory/internal/frick-counter
the number of fricks that have been detected using the STT system managed by jill

#### jill/token-bank
tokens used to throttle jill
- clock-ins/coins
- clock-ins/last
- events/coins
- events/coins
- events/last

### stream/credits/raids

### pyramid_schemers

### stream_start

### wordcloud/raw/counts

###  REMOVE?
- [ ] swear-jar
- [ ] tts-state/filtered
- [ ] tts-bank
- [ ] bans/jill/1112386096
- [ ] tts-state/user-filter-bypass-tokens/

