GMTK_GameJam_2022 - Roll of the DiceR
=====================================

About the Game Jam
------------------
- [Rules and Details here](https://itch.io/jam/gmtk-jam-2022)
- [The theme is Roll of The Dice](https://www.youtube.com/watch?v=NiSa-D5wy18)

About the Game
--------------

You are the DiceR, a ball of knives. Your job is to make a stew. Roll over ingredients to dice them up and attach
them to your blades. You can shoot a knife out to grab distant ingredients or attach to walls. Once you have enough
ingredients, drop yourself into the pot to cook the stew.

Missing Features and other Suggestions
--------------------------------------

- Grapple Blade - The blade that points to the pot was originally supposed to be a grappy that could grab food or latch
  on to surfaces to help you turn.
- MagnatizeR (Martin) - A challenge involving magnets that pull on the metal DiceR
- ObliteRatoR (Martin) - Spinning obstacles that know you away 

### Controls

Keyboard + Mouse
- W S A D => Movement
- Hold Left Mouse Button => Fire a knife towards the mouse
- Release Left Mouse Button => Recall the blade (releasing any walls)

Dev Log
-------

### Day 3 - 15:00

I used Stylized Render System to cell shade everything, and it really looks much better (not great, I'm still no
artist), but I'm really happy with it. There is now what I would call a submittable version of it on itch.io.

### Day 3 - 12:40

With a little over 5 hours to go, I'm going to spend the next 3 hours polishing as much as I can, and then I'll use the
final 2 hours to make sure the itch.io page looks as good as possible.

I'm going to throw up a quick unpolished build and try to get some feedback too. Not a lot I can change now, but any
bugs still need to be squashed.

### Day 3 - 12:00

It's officially a game! There's a bug on the "Lose" menu that needs fixing, you have to press Escape to get out, the
back button doesn't work. Going to leave that for now and move on to polish, get it looking nice, see if I can add sound
effects.

### Day 3 - 10:10

Turns out making a font with a distance field in Unreal is really hard. I'll use Roboto for now and maybe come back to
that later. I also just had my first Editor crash, so you know it's the final hours of a competition. 😅

### Day 3 - 9:15

I have a plan for the map, it's not _very_ interesting, but it will do. If I had more time I'd add interactive elements
to the map, and it definitely would have been better to do either a golf style game with multiple simple maps or if the
throwing knife had worked, and I could use that for locomotion, but I'm happy with how much I've achieved by myself.

Lets get this map made!

### Day 3 - 8:50

Timer done and nicely presented. Need to shrink the pot's collision sphere as you can clip it while bouncing over the
pot. Also going to try to find all Rs and make them capitalised.

### Day 3 - 8:30

Time to wrap this up! The major goals for the day are getting the timer working, building a level, and getting a
tutorial in. I'm going to can the firing mechanism and have the extra knife point towards the pot. If there's time I
still need sound effects, music and game juice.

### Day 2 - 23:30

Ending a bit earlier tonight to try to rest up for tomorrow. Missing a timer, but otherwise the game is officially a
game with controls, a win state and a lose state (as well as scoring and a little humour thrown in for fun)

### Day 2 - 21:15

While I was walking over to the pop-up store I read up on the maths and it's actually pretty simple, I just need to
cross the normal of the plane with a vector pointing straight up, this produces a vector pointing across the plane.
Crossing that vector with the normal again gives me one that points down the plane. Then I can just apply a force along
that vector which is the mass multiplied by (1 - normal.z)

### Day 2 - 19:00

Ok, I realised that slopes weren't working correctly. I made a mistake using a character for the DiceR. The character
only reacts to slopes in one of two ways, it either is "walkable" in which case you can stand still on it, there's no
downward force, or its not walkable, in which case there is a downward force, but you can't move up it at all (even
though the character is not walking, they're being pushed around). I think I should be able to apply a downward force
myself, but the maths isn't working. I'm going to take a break for dinner and pop to a friends pop-up store.

### Day 2 - 15:42

Things are going well now. Food gets diced (needs juicing, stuff just appears) and I've sped up movement, and made the
ball roll down ramps. (Also my Deliveroo turned up 😂)

On to the UI

### Day 2 - 14:15

Due to an outage at Deliveroo, I had to walk to town to get some food. Minor set back. I'm having a little break from
the problem which I'm currently trying to solve, moving child actors into the world. For some reason destroying the
parent actor after detaching them still removes the children, even though they're in the world. Might just make the
parent invisible, or maybe once they're attached to the player the problem will go away.


### Day 2 - 12:05

Really proud of my dynamic food types. I should be able to add more if I like and only have to change one function
library. I can already tell the art style of this game will be terrible, but not likely much I can do about that. This
would look really nice with a cartoon-y cell shaded look.

### Day 2 - 11:00

Solved the problem with the DiceR not moving. It was something to do with using GameState as the parent of my GameState
rather than GameStateBase

### Day 2 - 10:25

While working on the pot logic, the DiceR stopped moving. No idea why, major set back. Thank goodness for git, I can
see it was something recent that broke, but I got into a bad habit of doing large commits so this'll set me back.

### Day 2 - 8:00

Woke up a bit earlier than I intended, 7:30, but I'm washed, watered and fed so its time to go. Going to start by
rethinking the way I've done my Trello Board. I want to concentrate on the very basic game (pick stuff off and drop it
off) first, adding the shooting mechanic after.

### Day 1 - Midnight

Time for bed! Got the motion down (needs a lot of tweaking), and have knife to use as a projectile facing toward the
mouse. Tomorrow I'll try to get the projectile firing and returning. Then we can start adding food.

### Day 1 - 21:24

I've got it!

I'm going to make a golf game. The hole will be a pot, the ball will be knives, and you have to chop up food for a stew
on your way around the course. More food is better taste, there's no limit to how many times you can hit the ball but
there are hungry customers waiting.

I've [created a Trello board](https://trello.com/b/ptV8qYoP/roll-the-dicer) to try to keep focused.

### Day 1 - 20:47

Found a good tutorial on making a rolling ball here: https://www.youtube.com/watch?v=Y69FOMRGwUs

Unfortunately my internet died while I was watching it.

### Day 1 - 19:34

Ok, I've had Pizza, and I've decided to get something rolling and see where it takes me. I'm still thinking "Roll of the
DiceR" but I don't know if the player is the DiceR, or the one at risk of being Diced.

### Day 1 - 18:10

Ok, no excessive gore. I'm not in it to win it, but I also do not want to get disqualified or cause people to be upset
and I myself find knives a bit difficult. Back to the drawing board. Not easy as I've not got stuck on that idea. I
could go very cartoon-y, maybe make the things you're cutting food, and it literally gets turned into small cubes.

No, that's silly. Let me think.

- A first-person shooter where your gun rolls a die when you reload?
- A first-person game where you throw dice, and they do something when they land depending on the face?
- A marble run with a chonky dice (lack of control might not be great fun)
- A tower defence game where you roll a die and have to place a random tower
- A luck pushing game where the more you roll the more you win but the more chance of losing

I keep coming back to the twin stick knife idea. A ball with knives on it, you can crash into enemies to kill them,
and shoot knives for far away enemies that maybe fire back?

Ok, going to make food and let the ideas stew.

### Day 1 - 18:05

The theme is roll of the dice. Anyone who knows me knows I love board games and TTRPGs... but I don't think I could make
anything like that for the Jam. I'm entering solo so I want something very simple. Right now I'm thinking, does "Dice"
need to be the numbered kind, or could it be dice like to cut. Right now, I'm thinking something like a ball with knives
but, I want to check the rules on violence, and I worry that knives can be quite triggering for some people.

### Day 1 - 17:55

Excite! Ok the plan is:

Day 1 (from 6pm): Ideate and plan
Day 2: Build a working game
Day 3 (until 6pm): Juice

### Day 1 - 17:35

Hello! I'm going to use this README to write up my process as I go along. So far, following the rules, I've prepped my
project and repository but haven't actually started work yet. Can't wait to find out what the theme is, though I
already have a vague idea of the genre I'm going to build around, twin stick shooter. Lets see how long that idea lasts
once the theme is announced.

I'm making all the code freely available here. My goal here isn't to make money, or get top 100, my hope is simply to
think of an idea, and deliver it on time. Fingers crossed!
