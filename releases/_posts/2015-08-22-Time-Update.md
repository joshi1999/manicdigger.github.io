There have been requests and rumors and here it finally is: **Manic Digger 2015-08-22**  
As usual quite a lot has changed since the last release.

This mostly is a bugfix release but also introduces some features long requested by the community.

## Adjustable ingame time
This certainly is one of the features asked for the most by the players.  
While it might seem simple it required quite some changes in how time is handled by the game. I won't bore you with the technical details.

### So it's here. Now how do I use it?
Changing the time of day is done using a *server command*.
It requires the privilege ***time***.
The easiest way to try this is entering the command on the server console.

#### Setting the time
You can directly set the game time by entering the following command where you replace `[time]` with an actual value.  
*Format is described below*

```
/time set [time]
```

Another possibility is adding (you can also add negative amounts) time to the current time.
This can be achieved by entering the following (replace `[time]` with an actual value).  
*Format is described below*

```
/time add [time]
```

As a nice bonus you can also modify the speed of time.
Simply enter the following (replace `[speed]` with an actual value).  
*Speed can be any integer.*

```
/time speed [speed]
```

#### Time format
Time is given in the following format:
```
(-)(d.)hh:mm:ss
```

```
d   : days    (0 to 10675199) [optional]
hh  : hours   (0 to 23)
mm  : minutes (0 to 59)
ss  : seconds (0 to 59) [optional]
```

Further explanation can be found [here](https://github.com/manicdigger/manicdigger/issues/107#issuecomment-72533357) and [here](https://msdn.microsoft.com/en-us/library/se73z7b9%28v=vs.90%29.aspx).

#### Querying current time
And here is an example of the simplest usage. Asking what time it is.  
*Please note that the server will also return the current time when entering an invalid command or you do not have the necessary privilege!*

```
/time
```

## A small change in system requirements
Manic Digger now requires **.NET 3.5** to start.
In fact, this requirement has already been here in the last release but has not been enforced.

As .NET 3.5 is out now for quite a while and supported on all major operating systems by either the official runtime or the one supplied by the Mono project this should not cause any real trouble.

## Fixed bugs
Several bugs occured in the last release that could be really annoying. Good news is we've taken care of those.  
So here's a list of the most important bugs fixed in this release.

#### The falling sound
I guess almost everyone has had the "pleasure" of hearing that lovely sound repeating forever when entering free move mode. This has been taken care of accordingly.

#### Ctrl-V in chat
This certainly was something that could get annoying easily if you wanted to send your friends that one special link...

#### Mushrooms growing through stairs
Maybe you never encountered this one but it really was a nasty one for me. Good thing we finally got around to fix it.

#### Terrain rendering bugs
The introduction of the new terrain renderer in the last release brought massive improvements in terms of code readability but also some graphical glitches.  
Most of these have been fixed. A few are still remaining and will be fixed later on.
