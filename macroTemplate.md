Roll20 Macros
=============
Roll Initiative
---------------
```
/me enters the fight!
&{template:default}{{name=::Initiative::}}{{Initiative Roll=[[1d20 + @{selected|initiative_bonus} &{tracker}]]}}
```
Attack Rolls
------------
#### Strength Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|strength_mod}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|strength_mod}]] vs. @{target|foe|npc_AC} AC}}
```
#### Dexterity Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|dexterity_mod}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|dexterity_mod}]] vs. @{target|foe|npc_AC} AC}}
```
#### Strength + Proficiency Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|strength_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|strength_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}
```
#### Dexterity + Proficiency Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|dexterity_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|dexterity_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}
```
#### Intelligence + Proficiency Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|intelligence_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|intelligence_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}
```
#### Wisdom + Proficiency Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|wisdom_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|wisdom_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}
```
#### Charisma + Proficiency Attack
```
/me attacks @{target|foe|character_name}!
&{template:default}{{name=::To Hit::}}{{attack=@{selected|token_name} [[1d20+ @{selected|charisma_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}{{Second Roll=@{selected|token_name} [[1d20+ @{selected|charisma_mod} + @{selected|pb}]] vs. @{target|foe|npc_AC} AC}}
```
Difficulty Checks
-----------------
#### Strength DC
```
/me makes a strength difficulty check
&{template:default}{{name=::Strength DC::}} {{[[1d20+ @{selected|strength_mod}]]}} {{[[1d20+ @{selected|strength_mod}]]}}
```
#### Dexterity DC
```
/me makes a dexterity difficulty check
&{template:default}{{name=::Dexterity DC::}} {{[[1d20+ @{selected|dexterity_mod}]]}} {{[[1d20+ @{selected|dexterity_mod}]]}}
```
#### Constitution DC
```
/me makes a constitution difficulty check
&{template:default}{{name=::Constitution DC::}} {{[[1d20+ @{selected|constitution_mod}]]}} {{[[1d20+ @{selected|constitution_mod}]]}}
```
#### Intelligence DC
```
/me makes a intelligence difficulty check
&{template:default}{{name=::Intelligence DC::}} {{[[1d20+ @{selected|intelligence_mod}]]}} {{[[1d20+ @{selected|intelligence_mod}]]}}
```
#### Wisdom DC
```
/me makes a wisdom difficulty check
&{template:default}{{name=::Wisdom DC::}} {{[[1d20+ @{selected|wisdom_mod}]]}} {{[[1d20+ @{selected|wisdom_mod}]]}}
```
#### Charisma DC
```
/me makes a charisma difficulty check
&{template:default}{{name=::Charisma DC::}} {{[[1d20+ @{selected|charisma_mod}]]}} {{[[1d20+ @{selected|charisma_mod}]]}}
```
Weapon Attacks
--------------
### Simple Melee
| Weapon        | Cost           | Damage  | Weight  | Properties       |
| ------------- |:--------------:| ------- | :-------: | ---------------- |
| Club | 1 sp | 1d4 bludgeoning | 2 lb. | Light |
| Dagger	| 2 gp |	1d4 piercing | 1 lb. | Finesse, light, thrown (range 20/60) |
| Weapon | Cost | Damage | Weight | Properties |
| Greatclub |	2 sp |	1d8 bludgeoning |	10 lb. |	Two-handed |
| Handaxe |	5 gp |	1d6 slashing |	2 lb. |	Light, thrown (range 20/60) |
| Javelin |	5 sp |	1d6 piercing |	2 lb. |	Thrown (range 30/120) |
| Light hammer |	2 gp |	1d4 bludgeoning |	2 lb. |	Light, thrown (range 20/60) |
| Mace |	5 gp |	1d6 bludgeoning |	4 lb. |	- |
| Quarterstaff |	2 sp |	1d6 bludgeoning |	4 lb. |	Versatile (1d8) |
| Sickle |	1 gp |	1d4 slashing |	2 lb. |	Light |
| Spear |	1 gp |	1d6 piercing |	3 lb. |	Thrown (range 20/60), versatile (1d8) |
#### Club
`&{template:default} {{name=Club}} {{Info=Light}} {{damage=[[1d4+@{strength_mod}]] Bludgeoning}}`
#### Dagger
`&{template:default} {{name=Dagger}} {{Info=Main Hand, Finesse, Light, Thrown}} {{range=20-60}} {{damage=[[1d8+@{dexterity_mod}]] Piercing}}`
#### Greatclub
`&{template:default} {{name=Greatlub}} {{Info=Two Handed}} {{damage=[[1d8+@{strength_mod}]] Bludgeoning}}`
#### Handaxe
`&{template:default} {{name=Handaxe}} {{Info=Light, Thrown}} {{range=20-60}} {{damage=[[1d6+@{strength_mod}]] Slashing}}`
#### Javelin
`&{template:default} {{name=Javelin}} {{Info=Thrown}} {{range=30-120}} {{damage=[[1d6+@{dexterity_mod}]] Piercing}}`
#### Light Hammer
`&{template:default} {{name=Hammer, Light}} {{Info=Light, Thrown}} {{range=20-60}} {{damage=[[1d4+@{strength_mod}]] Bludgeoning}}`
#### Mace
`&{template:default} {{name=Mace}} {{Info= }} {{damage=[[1d6+@{strength_mod}]] Bludgeoning}}`
#### Quarterstaff
`&{template:default} {{name=Quarterstaff}} {{note=Simple, Versatile}} {{damage=[[?{Versitile|One Handed,1d6+@{strength_mod}|Two Handed, 1d8+@{strength_mod}}]] Piercing}}`
##### or for DEX
`&{template:default} {{name=Quarterstaff}} {{note=Simple, Versatile}} {{damage=[[?{Versitile|One Handed,1d6+@{dexterity_mod}|Two Handed, 1d8+@{dexterity_mod}}]] Bludgeoning}}`
#### Spear
`&{template:default} {{name=Spear}} {{note=Simple, Versatile, Thrown}} {{range=20-60}} {{damage=[[?{Versitile|One Handed,1d6+@{strength_mod}|Two Handed, 1d8+@{strength_mod}}]] Piercing}}`
##### or for DEX
`&{template:default} {{name=Spear}} {{note=Simple, Versatile, Thrown}} {{range=20-60}} {{damage=[[?{Versitile|One Handed,1d6+@{dexterity_mod}|Two Handed, 1d8+@{dexterity_mod}}]] Piercing}}`

### Simple Range
| Weapon        | Cost           | Damage  | Weight  | Properties       |
| ------------- |:--------------:| ------- | :-------: | ---------------- |
| Crossbow, light |	25 gp |	1d8 piercing |	5 lb. |	Ammunition (range 80/320), loading, two-handed |
| Dart |	5 cp |	1d4 piercing |	1/4 lb. |	Finesse, thrown (range 20/60) |
| Shortbow |	25 gp |	1d6 piercing |	2 lb. |	Ammunition (range 80/320), two-handed |
| Sling |	1 sp |	1d4 bludgeoning |	- |	Ammunition (range 30/120) |
#### Crossbow, Light
`&{template:default} {{name=Crossbow, Light}} {{Info=Two-Handed, Loading}} {{range=80-320}} {{damage=[[1d8+@{dexterity_mod}]] Piercing}}`
#### Dart
`&{template:default} {{name=Dart}} {{Info=Finesse, Thrown}} {{range=20-60}} {{damage=[[1d4+@{dexterity_mod}]] Piercing}}`
#### Shortbow
`&{template:default} {{name=Shortbow}} {{Info=Two-Handed}} {{range=80-320}} {{damage=[[1d6+@{dexterity_mod}]] Piercing}}`
#### Sling
`&{template:default} {{name=Sling}} {{range=30-120}} {{damage=[[1d4+@{dexterity_mod}]] Bludgeoning}}`

### Martial Melee
| Weapon        | Cost           | Damage  | Weight  | Properties       |
| ------------- |:--------------:| ------- | :-------: | ---------------- |
| Battleaxe |	10 gp |	1d8 slashing |	4 lb. |	Versatile (1d10) |
| Flail |	10 gp |	1d8 bludgeoning |	2 lb. |	- |
|Glaive |	20 gp |	1d10 slashing |	6 lb. |	Heavy, reach, two-handed |
| Greataxe |	30 gp |	1d12 slashing |	7 lb. |	Heavy, two-handed |
| Greatsword |	50 gp |	2d6 slashing |	6 lb. |	Heavy, two-handed |
| Halberd |	20 gp |	1d10 slashing |	6 lb. |	Heavy, reach, two-handed |
| Lance |	10 gp |	1d12 piercing |	6 lb. |	Reach, special |
| Longsword |	15 gp |	1d8 slashing |	3 lb. |	Versatile (1d10) |
| Maul |	10 gp |	2d6 bludgeoning |	10 lb. |	Heavy, two-handed |
| Morningstar |	15 gp |	1d8 piercing |	4 lb. |	- |
| Pike |	5 gp |	1d10 piercing |	18 lb. |	Heavy, reach, two-handed |
| Rapier |	25 gp |	1d8 piercing |	2 lb. |	Finesse |
| Scimitar |	25 gp |	1d6 slashing |	3 lb. |	Finesse, light |
| Shortsword |	10 gp |	1d6 piercing |	2 lb. |	Finesse, light |
| Trident |	5 gp |	1d6 piercing |	4 lb. |	Thrown (range 20/60), versatile (1d8) |
| War pick |	5 gp |	1d8 piercing |	2 lb. |	- |
| Warhammer |	15 gp |	1d8 bludgeoning |	2 lb. |	Versatile (1d10) |
| Whip |	2 gp |	1d4 slashing |	3 lb. |	Finesse, reach |
#### Battleaxe
`&{template:default} {{name=Battleaxe}} {{note=Versatile}} {{damage=[[?{Versitile|One Handed,1d8+@{strength_mod}|Two Handed, 1d10+@{strength_mod}}]] Slashing}}`

#### Flail
10 gp	1d8 bludgeoning	2 lb.
#### Glaive
20 gp	1d10 slashing	6 lb.	Heavy, reach, two-handed
#### Greataxe
30 gp	1d12 slashing	7 lb.	Heavy, two-handed
#### Greatsword
50 gp	2d6 slashing	6 lb.	Heavy, two-handed
#### Halberd
20 gp	1d10 slashing	6 lb.	Heavy, reach, two-handed

#### Lance
&{template:default} {{name=Lance}} {{Info=Reach}} {{Special=You have disadvantage when you use a lance to attack a target within 5 feet of you. Also, a lance requires two hands to wield when you aren't mounted.}} {{damage=[[1d12+@{strength_mod}]] Piercing}}

#### Longsword
&{template:default} {{name=Longsword}} {{note=Versatile}} {{damage=[[?{Versitile|One Handed,1d8+@{strength_mod}|Two Handed, 1d10+@{strength_mod}}]] Slashing}}

#### Maul

10 gp	2d6 bludgeoning	10 lb.	Heavy, two-handed
#### Morningstar

15 gp	1d8 piercing	4 lb.	-
#### Pike

5 gp	1d10 piercing	18 lb.	Heavy, reach, two-handed

#### Rapier
&{template:default} {{name=Rapier}} {{Info=Finesse}} {{damage=[[1d8+@{strength_mod}]] Piercing}}
or for DEX
&{template:default} {{name=Rapier}} {{Info=Finesse}} {{damage=[[1d8+@{dexterity_mod}]] Piercing}}

#### Scimitar
&{template:default} {{name=Scimitar}} {{Info=Finesse, Light}} {{damage=[[1d6+@{strength_mod}]] Slashing}}
##### or for DEX
&{template:default} {{name=Scimitar}} {{Info=Finesse, Light}} {{damage=[[1d6+@{dexterity_mod}]] Slashing}}

#### Shortsword
&{template:default} {{name=Shortsword}} {{Info=Finesse, Light}} {{damage=[[1d6+@{strength_mod}]] Piercing}}
#### or for DEX
&{template:default} {{name=Shortsword}} {{Info=Finesse, Light}} {{damage=[[1d6+@{dexterity_mod}]] Piercing}}

#### Trident
5 gp	1d6 piercing	4 lb.	Thrown (range 20/60), versatile (1d8)
#### War pick
5 gp	1d8 piercing	2 lb.	-
#### Warhammer
15 gp	1d8 bludgeoning	2 lb.	Versatile (1d10)
#### Whip
1d4 slashing	3 lb.	Finesse, reach

### Martial Ranged
| Weapon        | Cost           | Damage  | Weight  | Properties       |
| ------------- |:--------------:| ------- | :-------: | ---------------- |
| Blowgun |	10 gp |	1 piercing |	1 lb. |	Ammunition (range 25/100), loading |
| Crossbow, hand |	75 gp |	1d6 piercing |	3 lb. |	Ammunition (range 30/120), light, loading |
| Crossbow, heavy |	50 gp |	1d10 piercing |	18 lb. |	Ammunition (range 100/400), heavy, loading, two-handed |
| Longbow |	50 gp |	1d8 piercing |	2 lb. |	Ammunition (range 150/600), heavy, two-handed |
|Net |	1 gp |	- |	3 lb. |	Special, thrown (range 5/15) |
#### Blowgun
10 gp	1 piercing	1 lb.	Ammunition (range 25/100), loading
#### Crossbow, hand
75 gp	1d6 piercing	3 lb.	Ammunition (range 30/120), light, loading
#### Crossbow, heavy
50 gp	1d10 piercing	18 lb.	Ammunition (range 100/400), heavy, loading, two-handed

#### Longbow
&{template:default} {{name=Shortbow}} {{Info=Heavy, Two-Handed}} {{range=150-600}} {{damage=[[1d8+@{dexterity_mod}]] Piercing}}

#### Net
```
&{template:default} {{name=Net}} {{Info=Special, Thrown}} {{range=5-15}} {{damage=A Large or smaller creature hit by a net is restrained until it is freed. A net has no effect on creatures that are formless, or creatures that are Huge or larger. A creature can use its action to make a DC 10 Strength check, freeing itself or another creature within its reach on a success. Dealing 5 slashing damage to the net (AC 10) also frees the creature without harming it, ending the effect and destroying the net. -- When you use an action, bonus action, or reaction to attack with a net, you can make only one attack regardless of the number of attacks you can normally make.}}
```
	1 gp	-	3 lb.	Special, thrown (range 5/15)
