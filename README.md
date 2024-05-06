# MC-server-assistant-Discord-bot
Discord bot to give your players commands to interact with a Minecraft game server.

This bot aims to give players basic commands related to the server status and also give them a way to interact with the role-play game, based on the context of a cooperative town in game.



Firstly, we will see the generic commands:

...: Check server status (Online, Waiting*, Offline)
...: Get server IP
...: Try to turn on the server if it's offline.

* Waiting status means the game server is not fully online and playable, but can be started automatically when any players tries to enter it.
  This state is only achivable if 'MC-server-starter' has been installed and is being used to keep the server waiting.



Secondly, we will take a look ar the role-play specific commands:

The Minecraft server can be in survival or creative, but this bot is made to assist a survival server. In game, a group of players, we'll refer to them as 'citizens', will live in a town and cooperate.
  Cooperation will not be forced nor obligatory, but it's necessary that citizens don't want to destroy each other (although pranks may be allowed). 
  It's recommended to set a plugin or mod to allow players to protect the chunks inside the town where they have built something.
    Similarly, it's recommended to protect the 'common' chunks, or palces in the town made to be used by all the citizens (such a tonwhall).

We will distinguish 5 types of players inside the server: 'player', 'citizen', 'mod', 'major' and 'admin'. Here's a description of every one:
- player: basic role. Doesn't have access to the town where players cooperate (it's useful to set a requirement for new players before they become citizens.
- citizen: has access to the town, which means they can vote for the major and also apply for the position.
- mod: has special abilities inside the server (they should also be mods in any Discrod server related, or similars). Can kick / ban players.
- major: role purely made for the role-play: has special permissions in the city, such as proposing new common buildings, or modifying rules inside the city.
- admin: abosulte supervisor, has all privilegies. Always makes sure all the other players aren't causing problems.

Players can interact with the role game without the need to enter the game server.

...: Apply as a major for the next ellections.
...: Vote for a specific player to be the next major.


Some thinhs done in the background:

Every week (a specific day of the week at a specific hour), the major will lose it's title and the next ellections will begin with all the players who have applied.
  If only one player has applied, he will be automatically be announced as the next major.  
  If no player has applied, the defalut-major (should be an admin) will be assigned until any other player applies as a major, then, this player will become the major until the next auto reset.



Now, the admin has to configurate some things:
- IP of the Minecraft server
- in-game name of every citizen (they can be asked to write it by themselves)
- Day and hour of major reset
- Manually give each player the citizen role when achieved.

