# vlc-playlist-resumer
Hi~~

This is a simple playlist resumer that can create playlists and will resume them automatically.  
It depends on https://github.com/bellard/quickjs and also requires you to have write access to somewhere in /run.  
Also I used "notify-send" at one point, so that might be an issue.
Lastly, you will have to turn on the vlc console interface, otherwise it won't accept any commands.

The interface is rather simple.

`ivlc --help`  
will give you  
`create:,no-save,list,vlc-args:,help`  

`ivlc --list`  
shows you the playlists you already have  

`ivlc --create listName --vlc-args "--sub-track 2 --no-audio ..."  file1 file2 ...`  
will create a playlist that's always started with the given args  

`ivlc listName`  
will resume a certain playlist  

By default, ivlc will make whatever playlist you started or created last the default playlist that will be opened if you call ivlc without any args.
If you want to suppress that behavior, you can add `--no-save`.

It's still rough around the edges so will have to hack it a bit, but that's ok.

Bye
