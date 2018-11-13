=================================================================================
=========================== Hitman Twitch Assistant =============================
=================================================================================

Thank you for using the Hitman Twitch Steaming Assistant. You'll find a quick
start guide and specifics about each setting below.


================================== QUICK START ==================================

1. Open settings.json
2. Update username to match your name on Twitch (lowercase)
3. Update channelname to match your channel name on Twitch (should be the same, also lowercase)
4. Open https://twitchapps.com/tmi/ in a browser and log in using your Twitch account, copy password in full and paste it under password
5. Run the app, you can test it in your stream chat without streaming. Have fun!


================================= ADDING TO OBS =================================

This app is just like any game, so once you start it, you can add it to OBS (or whatever)
as a 'Game Capture', but window or display capture work as well.
From there you just need to add a Filter for Chroma Key to make the green background transparent


=================================== SETTINGS ====================================

//important settings//
"username"					- Your Twitch username (lowercase)
"password"					- Password can be obtained at https://twitchapps.com/tmi/ log in with your Twitch account.
"channelname" 				- Should be the same as your username, I think (lowercase).

//feature toggles//
"helpEnabled"				- enables "!help" and "!commands" commands in chat, these list the other commands for enabled features.
"thoughtsEnabled"			- enables thought bubbles to be used by typing "!think" or "!thought" followed by what agent 47 should think.
"soundboardEnabled"			- enables use of soundboard in chat. Can be accessed by "!say" followed by the phrase, or by putting the phrase in quotes. Full list at stealthkill.com
"killminigameEnabled"		- enables kill minigame (off by default). See explanation below this section.

//feature settings//
"thoughtsCooldown"			- cooldown (in seconds) for how often each viewer can use this feature (60 seconds by default).
"soundboardCooldown"		- cooldown (in seconds) for how often each viewer can use the soundboard (60 seconds by default).
"phraseComboLimit"			- when used in quotes phrases can be comboed indefinately (example "yea" "ok" "count it"). This setting limits the amount.

//kill minigame settings//
"killStartingThreshold"		- kill minigame thershold for bloodlust mode (101 by default). Setting it to 100 will allow a single viewer to trigger it, while more than that will require viewers to work together.
"killIncreaseWhenComplete"	- kill minigame thershold increase (1.1 by default). If set to 1, the threshold for bloodlust will not increase after a successful bloodlust run. If set to 2, it will double, etc.
"sacrificeTimer"			- determines how much time (in seconds) the streamer has to fulfill the sacrifice (default 100)

//other setting//
"rulesInterval"				- how often (in seconds) the rules are shown in chat (each hour by default)
"pingInterval"				- how often the chat is silently pinged for keepalive (60 seconds by default)


=========================== KILL MINIGAME EXPLAINED =============================

This little minigame is what set off my initial interest in creating this project
while the thoughts and soundboard aspect came later. It's basically a way for
your viewers to dictate when 47 needs to kill by working together as a group.

Rules: When a viewer types in "!kill" into the stream chat, 47's bloodlust goes up
by 100 points. The more viewers do this around the same time, the higher it goes up.

If the points go over the 'killStartingThreshold' (101 by default), 47 will go into
a blood rage state and a sacrifice is demanded. You (the streamer) will then have
100 seconds (by default) to kill someone in the game and then press:

[SPACEBAR] (assistant app has to have focus, though)

To confirm the kill has been made. If the kill is not made within the alotted time, 
the number of human sacrifices required doubles. Pressing [SAPCEBAR] is required
for each kill.

If all sacrifices are satisfied, you and your viewers win the minigame.

(This minigame feature is off by default because I feel it's kind of complicated
and having to focus on the app and push spacebar won't be viable for everyone.)


========================= NOTES AND RECOMMENDATIONS ============================

You'll probably want to use Low Latency streaming on Twitch to allow your viewers
a better chance at comedic timing. It's difficult with the Twitch delay being what 
it is.