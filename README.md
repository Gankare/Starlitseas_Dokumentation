# Filip Salomonsson - Some of my work on Starlitseas 
## Character movement and abillites
The character is half of the game, espacially in a parkour speedrun game. So I worked on the movement on and off the entire project, the movement script is pretty big so i wont go over it all. 

Image of whole player movement script:
![](/Assets/PlayerCharacter_WholeScript.png)

Making movement for jumping upwards on moving animated whales was hard, making it feel like the player is moving fast but still not making the game to hard. 

### Make the movement feel fast:
The script below is the update/tick event. To make the movement feel faster than it is, I added increassed fov and speed lines running down the screen when moving. 
![](/Assets/Update_PlayerScript.png)

### Whale tail jump:
When the whales are moving upwards their animated tails sometimes used to block the player from jumping onto the whales back. To fix this problem I added a tail jump I called ledgejump. When the player is holding space near a tail the player gets boosted into the air, like the tail is hitting the player upwards making the player be able to scale the whales instead of getting blocked by the tail and falling off. 

I put a collider check on the whales tails calling the players ledgejump script.
![](/Assets/Tailboost_WhaleScript.png)
When the players ledgejump script gets called, check if the player is holding space and if so do a tailjump.
![](/Assets/Ledgejump_Script.png)
I also made it look like a tail slap animation by speeding up the whales basic animation for one second when jumping on its tail. It looks like this: 
![](/Assets/TailJump.gif)

### Glide ability:

### Dash ability:

## Small features
### Fade in and out the whales: 
To many whales at the same time made the game lagg so I added render distance to the whales.
I thoght it looked wierd when they spawned in out of nowhere so I created a script that fades the material of the whales in and out:
![](/Assets/FadeScript.png)
![](/Assets/WhaleFade.gif)


### Blowhole water effect: 
When stepping on a blowwhales hole, the player gets shot up giving a speed boost. I added sound and made a water material to the boost for more of a feel.

I set the material the players screen for two secomds when steeping on the hole:
![](/Assets/BlowholeWaterEffect_Script.png)
It looks like this: 

![](/Assets/BlowHole_Gif.gif)

### Spirit Guide: 
I added a talking ray that gives the player tips on what to do or encourages the player to keep going every level. The text is a 3D widget set over the ray, the ray is always facing the player with the text. The text only shows when the player is close to the ray. 

Scipt of how this is done:
![](/Assets/TalkingRayScript.png)
The rays text is set in the level blueprint. You can see the sprirt guide in the leveldesign images below. 
![](/Assets/RayText_LevelBlueprint.png)

## LevelDesign
Starlitseas has 8 levels, every level going upwards towards heaven. I made the levels increasingly harder and longer, the whales are guiding the player towards haven. Adding different obsticles and changing the envoiroment to make every level special while keeping the same theme. 

The player follows the whales and floating islands throughout every level, the whales follows splines and thats how the levels are built. 

### Level 1: 
The first level starts at the beach and the bridge is higher than the player can walk, so the only way to get forward in the game is to learn to jump. there is also a spirit guide that shows the player the basic controls.

![](/Assets/Level1_Ingame.png)
Level 1 is straight forward with only whale sharks, making it hard to fail. The player learns to jump on whales that slowly moves forward.
![](/Assets/Level1.png)

### Level 2: 
The second level is slightly longer, moving upwards making it harder to jump on the whales, introducing blow whales that shoots the player in the air when walking on them.
![](/Assets/Level2_Ingame.png)
Still an easy level but introducing new elements.
![](/Assets/Level2.png)

### Level 3: 
The third level is an introduction level for the glide mechanic and boosting rings, the only way to get from one platform to another is to use the glider and the boosts. Making the player learn how to use the mechanic in different ways. 
![](/Assets/Level3_ingame.png)
There are no whales in this level to make the player focus on the new mechainc without being stressed by constantly having to move forward.
![](/Assets/Level3.png)

### Level 4: 
The fourth level combines the new mechanics with the whale jumping and it has two different ways of getting to the goal, one way faster than the other but more risky for the players that want to speedrun.

The level also has a new darker look, making it feel like your higher up than in previous levels.
![](/Assets/Level4_Ingame.png)
The level also introduces the first obsticle that can kill you, the jellyfish rings are at the end of the level and makes for a more interesting gameplay, having to glide through them.
![](/Assets/Level4.png)

### Level 5: 
The fifth level is pretty straight forward, The splines are tight together with alot of obsticles to make it slower and harder for the player to go around them.
![](/Assets/Level5_Ingame.png)

![](/Assets/Level5.png)

### Level 6: 
The sixth level is an introduction level for the dash mechanic, the look of the level is lighter with an aurora and fantasy feel, to create the feeling of heading towards space/upwards. 

I also added the giant whale in the background to add to the fantasy feel. The giant whale slowly goes around the map with the help of a rotating springarm set in the middle of the map.
![](/Assets/Level6_Ingame.png)
The level is like the third level but harder. It takes a combination of all the mechanics to beat it, this level is where most players gets stuck a while and it's to makes the player ready for the last two levels.
![](/Assets/Level6.png)

### Level 7: 
The seventh level is the longest one, it has two possible paths for the player to go right from the start, one faster than the other. There is a bunch of gliding in this level and it gives of a magical/fantasy feeling.

Midlevel there is a giant leap of faith, fog should be hiding the islands ahead (not like in the image below), making the player glide into the fog then revealing a bunch of islands with whales souring around them. Giving the player an epic feeling. 
![](/Assets/Level7_Ingame.png)
![](/Assets/Level7_Glide.gif)
![](/Assets/Level7.png)

### Level 8: 
The eight level is the last level before arriving in heaven. Whales flying in every direction and then going down again giving the feeling they have reached their destination, leading the player towards the sky. This is the most magical looking level.

To get to the end the player has to jump and dash from island to island, every island higher than the last, reaching the top taking them to heaven and clearing the game. 
![](/Assets/Level8_Ingame.png)
![](/Assets/Level8.png)
