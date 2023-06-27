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
from keep_alive import keep_alive


intents = discord.Intents.default()


client = commands.Bot(command_prefix=':', intents=intents, self_bot=True, help_command=None)


GUILD_ID = 852009601222049834
CHANNEL_ID = 1022568912262545448

@client.event
async def on_ready():
    os.system('clear')
    print(f'Logged in as {client.user} ({client.user.id})')
    vc = discord.utils.get(client.get_guild(GUILD_ID).channels, id = CHANNEL_ID)
    await vc.guild.change_voice_state(channel=vc, self_mute=True, self_deaf=True)
    print(f"Successfully joined {vc.name} ({vc.id})")

keep_alive()
client.run(os.getenv("TOKEN"))

```

[Support Server](https://dsc.gg/parisa).

**DO NOT GIVE YOUR TOKEN TO OTHERS!**

Use [uptimerobot.com](https://uptimerobot.com) to make your repl online 24/7.

</br>

> ⭐ Feel free to star the repository if this helped you! ;)

----

> Voicecord by Alkhazalih is licensed under Attribution 2.0 International 
