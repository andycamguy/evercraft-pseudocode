# What am I doing?

I am not sure but here we go.

**Use OOP and Test-Driven Development to create the backend of an RPG character like that of Dungeons and Dragons or the MMO Everquest, but it is called
Everquest

## Moscow
### Must Have
A Character created with Health, Armor, a name and Alignment based on the first Iteration from the Everquest Kata manual0
### Should have
Iteration 2 from the Everquest Manual
### Could Have
Iteration 3 from the Everquest manual
### Won't Have
* Starcraft
* Fully working Campaign
* a hard coded dice (thanks clayton jk)

## Procedural Pseudocode

### Begin

### Initialize: set up the variables

- The character name, its starting attributes from the kata like dexterity, strength, intelligence, etc.
- A character's ability to attack and defend itself from the enemy
- modifiers for attributes
### Render
### Compute
the math for hitting an enemy using probability from a d20
the math for getting hit using probability from a d20
The modifiers alongside a hit with the modifier table provided that is embedded into the system
### END

## Functional
### Iteration 1 :: This iteration covers core functionality for leveling, combat, and character attributes.
```
function CreateaCharacter {
# As a character I want to have a name so that I can be distinguished from other characters
# As a character I want to have an alignment so that I have something to guide my actions
# As a combatant I want to have an armor class and hit points so that I can resist attacks from my enemies
  if this is a character {
    choose an alignment of good, neutral or evil
    set the character armor as 10 and hitpoints as 5
    }
}


function CanAttack {
#As a combatant I want to be able to attack other combatants so that I can survive to fight another day

if attacking enemy -- does it hit within the paramters of a d20?
does the attack exceed the opponent's armor?
if it does, it hits
it it is a natural 20, it is a critical hit and doubles damage
}

function CanDefend or GetRekt {
#As an attacker I want to be able to damage my enemies so that they will die and I will live

if the character' armor is stronger than the attack from opponent --> no damage
    # probability is rng 1-20
if the character's armor is less than the attack --> 1 point of damage

if the roll from opponent is a 20 --> 2 points of damage
}

function ability modifier {
# As a character I want to have several abilities so that I am not identical to other characters except in name
# As a character I want to apply my ability modifiers improve my capabilities in combat so that I can vanquish my enemy with extreme prejudice

-- invoke the can attack funtion
-- invoke the ability function?
based on the results, add or subtract damage using the Character's natural score from the math formula :: Modifier = floor((Score - 10) / 2)
 
  The math behind the modifier table involves a linear relationship between the score and the corresponding modifier. In this case, the relationship can be      described using a simple formula:


}

function gain experience {
# As a character I want to accumulate experience points (xp) when I attack my enemies so that I can earn bragging rights at the tavern
if opponent defender = dead
experience = experience + the amount gained from the opponent (in this case 10 xp)
}

function level up{
# As a character I want my experience points to increase my level and combat capabilities so that I can bring vengeance to my foes
if lvl = 1
xp gauge = lvl * 1000

}
```


### Iteration 2 Classes that a character can have.
```
classes = ( "barbarian", "bard", "cleric", "druid", "fighter", "monk", "paladin", "ranger", "rogue", "sorcerer", "warlock", "wizard")
# As a player I want a character to have a class that customizes its capabilities so that I can play more interesting characters
function pick a class {
input(pick a class or be a loser:)
charcter.class  = input
gain inherent values based on class

invoke inherit class function

}

function inherit class{
if class is within the classes array, add said values to the character values

# Fighter // As a player I want to play a Fighter so that I can kick ass and take names
10 add health per level up instead of 5 
dice roll = dice roll +1

# Rogue // As a player I want to play a Rogue so that I can defeat my enemies with finesse
automatically sets alignment to either neutral or evil
defender.dexterity.modifier = defender.dexterity
strength.modifier = dexterity.modifier
if roll = 20 damage is 3 times instead of 2 times

# Monk // As a player I want to play a Monk so that I can enjoy being an Asian martial-arts archetype in a Medieval European setting
6 add health per level up instead of 5

if can attack {
  3 points of damage instead of 1
  }
armor_class = wisdom.modifier only if it is greater than 0
attack roll is increased by 1 every 2nd and 3rd level

# Paladin // As a player I want to play a Paladin so that I can smite evil, write wrongs, and be a self-righteous jerk
#The oath of throwing it back is great with us
8 add health per level up instead of 5
+2 to attack and damage when attacking Evil characters
does triple damage when critting on an Evil character (i.e. add the +2 bonus for a regular attack, and then triple that)
attacks roll is increased by 1 for every level instead of every other level
can only have Good alignment
# Bard // As a player I want to play a Bard so that I can charm, inspire, and entertain my allies
8 add health per level up instead of 5
can cast one additional spell per level
can use Bardic Inspiration ability twice as many times per short rest







}
```
