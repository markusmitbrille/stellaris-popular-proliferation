Outdated as of Nemesis, as this expansion introduces logistic pop growth.

# Popular Proliferation
Overhaul to population growth and management.

While there are many mods that overhaul pop growth and management, I wanted to give it a shot too. I wanted to make growth natural, migration useful and job management fun, using only vanilla mechanics, while staying true to how I think the devs wanted them to work.

This mod does four main things:

+ Organic pops increase growth speed, the poorer they are, the greater the effect.
+ Robotic pops give new assembly jobs per pop. This requires an assembly building.
+ Overcrowding now only reduces growth/assembly speed (and immigration pull), it should and will occur.
+ Population control decisions are now actually useful and desirable.

## Gameplay Changes
### Growth and Assembly Speed
Growth and assembly have been overhauled so they will roughly result in a natural growth curve.

Organic pops breed - the more pops there are, the more they can breed, leading to exponential growth. This growth is stifled by wealth and housing. Wealth is represented by pop categories: Rulers and specialists still increase growth, but less so, while workers and slaves tremendously increase growth; in hive-minds complex drones act similarly to rulers and specialists, since their jobs are more demanding and they cannot focus on reproduction as intensively as menial drones. This adds an element of balance to managing organic populations: You want your pops to produce useful, high-level stuff like research, consumer goods and alloys, but the emerging middle-class on highly developed planets causes growth to stagnate. One way to keep such planets growing is immigration - just provide free housing and jobs and they will come.

Robotic pops are built by other pops, a process that has an overhead of quasi-useless pops that don't add any value to society, except for making new robots, but on the upside this means that robotic populations are not dependent on an impoverished lower class to continue growth. Assembly buildings now add additional assemblers, roboticists for mechanical and synthetic empires, replicators for machine empires, based on population, making them invaluable for worlds where exponential assemblage is desired.

Housing has been revamped: Going into red housing is a thing that should happen now and the only negative effect is that growth and assembly will start to go down, along with immigration pull. Growth and assembly will slow down to 0% when the required housing reaches 200% of the provided housing. Note that this doesn't mean planets will be able to house double the amount of people now, since housing requirements have been doubled as well on a pop by pop basis. At exactly zero free housing, growth will be at its highest, since population is at the largest, providing the greatest speed increase, right before growth reduction from crowding kicks in.

This might be the point to enable population controls and send all that delicious growth to other planets that have trouble growing on their own.

### Migration
Migration push and pull have been rebalanced. The most common source of immigration pull will be free jobs, while free housing and high stability will act as a multiplier. Emigration push, aside from unemployment and low stability, which are both undesirable, will now come from political decisions: Discrourage Growth and Population Controls are similar decisions that cause massive emigration push, at the cost of happiness and, in case of the former, increased upkeep. This makes it easy to stop planetary growth (mostly) without wasting it, while still maintaining a fun challenge - will you go for costly, but more popular growth discouragement or hardcore population controls? Gestalt empires have their own decision that is more efficient, simply because hive-minded pops don't seem to *mind* the totalitarian control over their lives.

Since robots don't migrate, they have their own mechanic added to the game via a harmless event that resettles newly assembled pops from planets with either gestalt population controls (for machine pops) or rerouted robot assembly (robots in normal, synthetic and mechanical empires) onto planets without such a modifier, the latter being added by another decision.

The decisions mentioned above no longer reduce or even completely stop pop growth or assembly.

### Abduction
One minor addition this mod makes, is that it includes a small decision to designate "Purge Worlds". When you abduct a pop, it will be settled on a random world with this modifier, provided there are any in your empire. This should make it easier to play a xeno-abducting purifier who only snatches poor aliens to work them to death on thusly named purge worlds.

## Balancing
For balancing refer to this extensive [spreadsheet](https://docs.google.com/spreadsheets/d/1kbdyD52Vk_0aKVh1qNB1TXWGevJIUIEH8djyTciL-S8/edit?usp=sharing).

## Compatibility
This mod should be compatible with most other mods, however if another mod makes changes to the same game element (like a building) they will overwrite each other, depending on your load order.

## Overwrites
A few vanilla files had to be overwritten, i.e. pop categories. Just overwriting the pop category elements broke all modifiers for pop categories, like "pop_cat_worker_happiness".

The following vanilla *files* have been overwritten:

+ Pop Categories:
  + 00_social_classes.txt
  + 01_gestalt_drones.txt
  + 02_other_categories.txt

The following vanilla *elements* have been overwritten:

+ Buildings:
  + building_robot_assembly_plant
  + building_machine_assembly_plant
  + building_machine_assembly_complex
+ Defines:
  + OVERCROWDING_NO_GROWTH_THRESHOLD
  + OVERCROWDING_DECLINE_THRESHOLD
  + BASE_POP_GROWTH
  + REQUIRED_POP_GROWTH
  + BASE_POP_ASSEMBLY
  + REQUIRED_POP_ASSEMBLY
  + MAX_EMIGRATION_PUSH
  + MAX_GROWTH_FROM_IMMIGRATION
  + MAX_GROWTH_PENALTY_FROM_EMIGRATION
+ Game Rules:
  + can_pops_grow_on_planet
  + can_pops_assemble_on_planet
+ Modifiers:
  + planet_housing_no_happiness_low
  + planet_housing_low
  + planet_housing_no_happiness_high
  + planet_housing_high
  + planet_overcrowded
  + planet_stability_low
  + planet_stability_high
  + planet_growth_discouraged
  + planet_population_control
  + planet_population_control_gestalt
  + planet_robot_assembly_control
+ Events:
  + id [action.121]
+ Localisations were overwritten accordingly.
