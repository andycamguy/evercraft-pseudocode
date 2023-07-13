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

## Fumctional

```
function CanAttack {
if attacking enemy -- does it hit within the paramters of a d20?
does the attack exceed the opponent's armor?
if it does, it hits
it it is a natural 20, it is a critical hit and doubles damage
}
```


