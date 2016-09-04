#FORGE OF EMPIRES helper a.k.a. **GLAVATY**
While playing FOE (forge of empires) I always needed to do calculation on how much FP must I invest in GB (great building) to overtake some position/rank and how much profit will I make. I also had problems when viewing "List of GB's you are contributing to", because I didn't know which GB's have progressed since my last visit. Based on that I decided to write this FOE helper, which I named **`GLAVATY`**, that will do all of the above and much more. But before I started programming, I did contact FOE support and asked them for blessing, because I didn't want to break any of the rules, especially the rule [6) Bots and scripts](https://en.forgeofempires.com/page/the_game/rules/). I did receive a response, that was a "go go go" for me:

> If you are only gathering data and displaying it in a different way, this would be allowed. However any automated process that directly effects a game mechanic or the way it would normally function with just normal user input, then this would be considered a violation as a bot or script.
What you are describing sounds like only a display enhancement, so it should not be a problem.

#**GLAVATY**

Let's write what it is currently done, will be done, might be done, will not be done...

###Implemented:

 - Can be used for all worlds, on all servers, at the same time!

 - Your every friend, neighbor and guild member score + last change date will be auto saved to DB. We will need this info for activity status, since we don't want to donate FP to GB who's owner is not active for month, or do we?

 - When you visit GB construction and rewards are available, they will be auto saved to DB. We will need this info for reward calculations. We could get this info from [wiki GB list](http://forgeofempires.wikia.com/wiki/Category:Great_Buildings), but there is a lot of missing data, especially for levels +30). So why not have a auto-learn option?

 - Your Arc bonus is auto saved to DB. We will need this info for reward calculations.

 - When you visit a player's town, GB's that have next requirements bellow, will be listed:
	 - if GB is leveled more than 50%:
		 - ![enter image description here](http://i.imgur.com/4i7oSpb.png)
	 - if you have invested in this GB:
		 - ![enter image description here](http://i.imgur.com/gsxZeuz.png)
		 - ![enter image description here](http://i.imgur.com/NOUfn5U.png)
	 - if GB contribution has changed since last visit:
		 - ![enter image description here](http://i.imgur.com/kkw6RXv.png)

 - When you visit a global ranking GB list, you get the same output as if you visit a player's town, with the difference:
![enter image description here](http://i.imgur.com/V4xbBI2.png)
	 - show only player's GB that you can contribute to (friends, neighbors, guild members);
	 - show only those that have changed since last visit;
	 - show only those that are not secured (do not show GB's where you already secured a rank; what for?).

 - When you visit your GB contribution list, you get the same output as if you visit a player's town, with the difference:
	 - show only those that have changed since last visit;
	 - show only those that are not secured (do not show GB's where you already secured a rank; what for?).

 - When you visit a GB construction you get next possible results/calculations:
	 - overtake rank with earnings:
		 - ![enter image description here](http://i.imgur.com/rJhkb85.png)
	 - overtake rank with loss:
		 - ![enter image description here](http://i.imgur.com/PixgJ3z.png)
	 - rank is secured:
		 - ![enter image description here](http://i.imgur.com/wcrjCCN.png)
	 - no action available:
		 - ![enter image description here](http://i.imgur.com/1Hkzm3d.png)
		 - ![enter image description here](http://i.imgur.com/l4Mc8rf.png)
		 - ![enter image description here](http://i.imgur.com/hnFNk55.png)
		 - ![enter image description here](http://i.imgur.com/wSNjD11.png)
		 - road missing etc...
		 - and so on...

 - When you contribute to GB, FP status of the GB is saved to DB, so next time you visit a player, GB ranking list or GB contribution list, you are shown the list of GB's that have changed from your last visit:
![enter image description here](http://i.imgur.com/lmNeWCq.png)


###Wish list:

 - Beep:
	 - when you get a message
	 - when you are attacked on GvG
	 - etc?

 - System notification, like windows toast etc.

 - WEB server with clean design; CLI is probably not for every1 :D
