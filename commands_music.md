# Music category
This can be accessed via `d.help Music` (please note the capital letter)

Reminder: commands are called with the prefix `d.`

I'll be honest, dudes... The libraries I use get updated a lot. Often one library is updated but another is not. When this happens, the bot shits itself and doesn't play music right. When this happes, just tag me (Mask) and say the bot harfed. The programmers generally fix this in a few days. I have no control over this. *sigh*

Generally speaking, you can start playing music by doing the following:  
  1. Join the voice channel called `music`
  1. In `#voice-text` type `d.connect music`
  1. Enter something like `d.play louis armstrong wonderful world`
  1. Enjoy the soothing sounds

## Commands in the Music category:
  connect, now_playing, play, pause, queue, resume, skip, stop, volume

Most of these have shorter aliases. Because it sucks to type a long-ass command. The `play` command is shown last because it has a long description. You'll see.

**connect [channel]**  
*alias:* join  
Usually the `play` command works without this first, but... I dunno. I've seen it fuck up without it. So just type `d.connect music` and you'll be fine.

**now_playing**  
*aliases:* np, current, currentsong, playing  
Display information about the currently playing song.

**pause**  
Pause the currently playing song. Use `q` instead.

**queue**  
*aliases:* q, playlist  
Retrieve a basic queue of upcoming songs. Save your sanity.

**resume**  
Resume the currently paused song.

**skip**  
Skip the song. Right now, anyone can skip. Let's be respectful and friendly. Friends don't let friends skip for no reason. Even the Eagles.

**stop**  
Stop the currently playing song & destroy the player. ***!Warning!*** This will destroy the player, also deleting any queued songs and settings.

**volume \<vol>**  
*aliases:* volume, vol  
Change the player volume. Can be a float or int in percentage. Must be between 1 and 100.


**play \<search>**  
*aliases:* sing  
Request a song and add it to the queue. This command attempts to join a valid voice channel if the bot is not already in one. (So just use `d.connect music` to speed this up. Thanks.) Uses YTDL to automatically search and retrieve a song.

You can specify a YouTube parameter. For instance, if the link is <https://www.youtube.com/watch?v=YedqV4Gl_us>, you can use `d.play YedqV4Gl_us` to request this audio.

You can also use a search, like `d.play louis armstrong wonderful world`

Now, dudes... Some of you will notice it uses the YTDL library. That supports Vimeo, Vevo, SoundCloud, and many more. There's a [complete list here](https://github.com/ytdl-org/youtube-dl/blob/master/docs/supportedsites.md) that you can look through if you're really bored. *Let's not put in X-rated audio, OK?* I'd hate to add a new rule. 

