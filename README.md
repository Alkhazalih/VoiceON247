# VoiceON247
Make your discord account 24/7 online on voice channels!

-------

A code written in Python that helps you to keep your account 24/7 on discord voice channels.

#### Developer Page: [sanad.mrtwix.repl.co](https://sanad.mrtwix.repl.co)

-------
Main.py File :
</br>

```py
import discord
import os
from discord.ext import commands

client=commands.Bot(command_prefix=':', self_bot=True, help_command=None)

GUILD_ID = YOUR_GUILD_ID_HERE
CHANNEL_ID = YOUR_CHANNEL_ID_HERE

@client.event
async def on_ready():
    os.system('clear')
    print(f'Logged in as {client.user} ({client.user.id})')
    vc = discord.utils.get(client.get_guild(GUILD_ID).channels, id = CHANNEL_ID)
    await vc.guild.change_voice_state(channel=vc, self_mute=True, self_deaf=True)
    print(f"Successfully joined {vc.name} ({vc.id})")

client.run(os.getenv("TOKEN"))
```

[Support Server](https://dsc.gg/parisa).

**DO NOT GIVE YOUR TOKEN TO OTHERS!**

Use [uptimerobot.com](https://uptimerobot.com) to make your repl online 24/7.

</br>

> ⭐ Feel free to star the repository if this helped you! ;)

----

> Voicecord by Mrtwix450 is licensed under Attribution 2.0 International 
