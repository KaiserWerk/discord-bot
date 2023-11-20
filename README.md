# discord-bot

Create a discord bot which can only be operated from a certain usergroup which you can select in the bots config.

This bot is supposed to write a log into a certain discord channel which can also be selected in setup.

What this bot is supposed to do is, it shall message server members which got assigned a specific role (This role can also be defined in setup).

The message it writes to the servermember is supposed to be customizable in the config, and it will have a keyphrase which is also customizable.
Same with the missed attempt message.

The bot then is supposed to say to the user the custom text. it is important, that in the custom text the variable <keyphrase> can be used, and the keyword will then be implemented into the text.



For example:

Custom Text:
Welcome to our discord! This is just a check if you're a bot.
Please answer with: <keyphrase>
Thank you for keeping our discord save!

The keyphrase being: i am not a bot

The endresult shall then be:

Welcome to our discord! This is just a check if you're a bot. Please answer with: 
i am not a bot
Thank you for keeping our discord save!




Then the bot waits for the user to reply with exactly the keyphrase.
If the user replies with anything other then the keyphrase, the bot will say the custom text which has been configured in the missed attempt config text.
For example "please only answere with the exact words: <keyphrase>" also with the functionality of the variable.

If the user has not replied within a time which can also be customized in the bots config, the bot will take action. The action it takes, will be defined in the config aswell , and can either be to message a certain person in a DM, ping a certain person or group in a server channel, just document that the user has failed to reply within the given time, automatically kick the user, or automatically ban the user from the discord server. It is always supposed to document its action taken, regardles which setting here is used.


If the user manages to reply in time with the correct keyphrase the bot will then write a success promt which can be customized in the config.
The bot then will document which user has passed the check and remove the discord role which promted it to check the user. The bot will also remember that this user has already been checked and will instandly remove the role if the same user gets that role assigned again, and then log a message saying that user XXX has already been checked at date X.
