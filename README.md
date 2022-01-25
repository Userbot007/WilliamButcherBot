
        </a>
    </p>
</h1>

<h1>
    <p align="center">
        <a href="https://heroku.com/deploy?template=https://github.com/Userbot007/WilliamButcherBot">
            <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
        </a>
    </p>
</h1>

<h3 align="center"> 
   Generating Pyrogram Session For Heroku
</h3>

```console
thehamkercat@arch:~$ git clone https://github.com/thehamkercat/WilliamButcherBot
thehamkercat@arch:~$ cd WilliamButcherBot
thehamkercat@arch:~$ pip3 install pyrogram TgCrypto
thehamkercat@arch:~$ python3 str_gen.py
```

<h1 align="center"> 
   ⇝ Docker ⇜
</h1>

```console
thehamkercat@arch:~$ git clone https://github.com/thehamkercat/WilliamButcherBot
thehamkercat@arch:~$ cd WilliamButcherBot
thehamkercat@arch:~$ cp sample_config.env config.env
```

<h3 align="center"> 
    Edit <b> config.env </b> with your own values
</h3>

```console
thehamkercat@arch:~$ sudo docker build . -t wbb
thehamkercat@arch:~$ sudo docker run wbb
```

<h2 align="center"> 
   ⇝ Write new modules ⇜
</h2>

```py
# Add license text here, get it from below

from wbb import app # This is bot's client
from wbb import app2 # userbot client, import it if module is related to userbot
from pyrogram import filters # pyrogram filters
...


# For /help menu
__MODULE__ = "Module Name"
__HELP__ = "Module help message"


@app.on_message(filters.command("start"))
async def some_function(_, message):
    await message.reply_text("I'm already up!!")

# Many useful functions are in, wbb/utils/, wbb, and wbb/core/
```

<h3 align="center"> 
   And put that file in wbb/modules/, restart and test your bot.
</h3>
