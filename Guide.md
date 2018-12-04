# Raidbots: A Guide

## What is Raidbots?
Raidbots is a website that runs SimulationCraft in the cloud. The website presents a Graphical User Interface (GUI) that allows for a simple visual version of SimulationCraft.

#### What is SimulationCraft?
SimulationCraft is an open-source project that uses action lists to simulate events and model player damage. By using action lists and specified event parameters, SimulationCraft is able to number crunch specific in-game scenarios.

#### What can SimulationCraft do?
While the possibilities are massive, the "normal" uses of SimulationCraft (SimC, from here forward) include DPS calculations, stat weights, and simulating hypothetical talent/gear combinations. By using this software, it is possible to determine the best items, talents, or gear for a character based on specific scenarios.

#### What's the difference between Raidbots and SimulationCraft?
Raidbots is a web based option to use SimC. Using SimC software to run simulations on a user's computer can be extremely taxing on the hardware depending on what simulations are done. Raidbots presents a solution to this by running simulations on cloud servers. Using Raidbots is no more taxing than using Google or any other website because the heavy lifting is done behind the scenes by servers instead of a user's own computer.

Raidbots also allows users to disregard updating and reinstalling SimC every update and even allows for the choice between Nightly or Weekly builds of SimC.

#### Using Raidbots with the addon "SimulationCraft"
SimulationCraft offers an in-game addon for World of Warcraft that makes using Raidbots a bit more simple. Downloadable through the Twitch app or the Curse website, SimulationCraft's addon (conveniently titled "Simulationcraft") allows for a large text output, brought up in-game in a unique window via the "/simc" command. The text generated takes a snapshot of the character logged in on, including their equipped gear, enchants, gems, talents, and even the gear in their bag. Copying this text in-game and pasting this into the "LOAD FROM SIMC ADDON" window on Raidbots' website loads a character's data at the very moment into Raidbots instead of relying on Blizzard's Armory API to update (which requires a logout and comes with a minor delay to update, and does not allow for usage with Top Gear, as that relies on in-bag items).

## What can Raidbots simulate?
Raidbots has 6 primary simulation options, including:
#### Top Gear
Top Gear allows users to simulate all item combinations from the items currently equipped and in the character's bag.
</br>
*Note: Requires SimulationCraft addon and output from in-game command "/simc" to be pasted into the text box on Raidbots' website.*
#### Gear Compare
Gear Compare allows users to simulate hypothetical item upgrades against the items the character currently has equipped. This feature includes a search option to look up any item and simulate a character using the new item, regardless of whether the character owns the item in game.
#### Talent Compare
Talent Compare allows users to simulate talent options versus the currently selected talents. This option allows for several talent builds to be compared.
#### Quick Sim
Quick Sim allows users to simulate a basic DPS value based on fight parameters using a character's current talent and gear composition.
#### Stat weights
Stat Weights allows users to simulate value of every primary and secondary stat based on a character's current talent and gear.
#### Advanced
Advanced allows users to run SimC scripts for custom priority lists or encounter parameters.

## Simulation Options
Raidbots allows for specific options to be modified for every type of simulation ran. These allow for specific tailoring of simulations based on the type of data desired--whether it's a short-lived single target encounter in a dungeon or a longer duration heavy add style fight in a raid, Raidbots has options that allow for simulating different styles of encounters.
#### Iterations
The iterations option is a way for a user to determine how many times the simulation is ran. The higher the iteration, the higher the number of times the simulation is ran, which creates more accurate data. There is also an option under iteration called "Smart Sim" which allows for a unique method of removing outliers and repeatedly simming at lower target error percentages to ensure results remain accurate without requiring a massive amount of iterations at a small target error. This allows for much more speed and less "work" for Raidbots to do while still remaining accurate in results.
#### Fight style
There are 9 fight styles available in Raidbots. This includes:
- Patchwerk
  - No movement, single target
- Hectic Add Cleave
  - Regular add spawns
    - 5 adds, 40% uptime
  - Frequent movement
- Light Movement
  - Infrequent Movement
    - 50 yards every 85 seconds
- Heavy Movement
  - Frequent Movement
    - 25 yards every 10 seconds
- Casting Patchwerk
  - Patchwerk that is always casting
    - Useful for simming interrupts
- Cleave Add
  - Single add spawn
    - 40% uptime
- Helter Skelter
  - Movement every 30 seconds
  - Interrupts every 30 seconds
  - Boss invulnerable every 120 seconds
- Beastlord
  - Boss with various add packs
    - Includes packs of melee mobs and pairs of ranged mobs
- Ultraxion
  - Single target
  - Player stuns & Raid damage

#### Number of Bosses
There are options for users to simulate between 1 and 10 bosses. This option can be changed regardless of fight style chosen.
#### Fight Length
There are options for 20 seconds, 40 seconds, and 1 to 10 minutes in 1 minute intervals.
#### SimC version
This option allows for users to use different builds of SimC. By using weekly, users have a higher chance of a successful simulation, while potentially missing recent hotfixes or changes. Nightly builds are more likely to include recent updates, but are also more likely to have bugs or failed simulations.
#### Raid Buff Presets
In Battle of Azeroth, specific classes have unique buffs, similar to previous expansions. Raidbots allows for users to pick and choose between specific buffs brought by individual classes depending on the composition of their party or raid, or allows users to assume they will have all buffs in their group.

## Simulation Guides

#### Top gear
The Top Gear functionality of Raidbots is by far the most involved and is able to give the most detailed output. By using the Simulationcraft addon and pasting a character's "snapshot," the interface on the Top Gear page changes. Top Gear allows for a user to simulate multiple items of gear, alongside enchant and gem preferences, and include multiple talent builds. By allowing this, a user is able to simulate potential upgrades based on if a certain group of items could result in a higher potential damage output, while taking into account for potential sockets on old or new items, enchants on items, and talents that may pull ahead based on item sets with different primary and secondary stat values.

###### Gear
Immediately under the paste window, the character's talents that are currently selected in-game are displayed. Below, there are two small checkboxes: "Hide Low Level Items" and "Hide Offspec Azerite Powers." Both of these options are checked by default, thereby hiding irrelevant gear and traits that are unavailable to be considered on Azerite gear that do not have any function for the current spec of the character. Further down begins the area where the character's currently equipped gear is shown, which is highlighted in an amber color, and gear the character owns but resides in the bag, which is shown without the amber border.

Azerite pieces (Head, Shoulder, Chest) all show their respective Azerite traits, including those selected on equipped pieces, separated by appropriate ring with light gray backgrounds between each set of choices in each ring. While in a specific spec, Raidbots only shows the usable traits for the primary row of Azerite--depending on the class and spec of the character, there may be between 2 and 4 traits available to choose for the first set of Azerite traits, while the standard is solely 2 traits available.

Gear options with more than one item, such as rings and trinkets, can be locked. By choosing to lock an item, it forces Raidbots to use the item and simulate other options for the secondary slot. For example, if a character owns 3 trinkets, a user can choose to lock trinket 1, allowing for 2 simulations: trinket 1+2 and trinket 1+3. By doing this, the total number of iterations can be lower due to less gear being simulated, while also allowing a user to keep an item that is potentially a known good item that should not be replaced by any other item.

###### Enhancements
Below the gear section resides the Enhancements section, which contains options for a character's enchantments and gems. By default, the MAIN HAND section, which shows weapon enchants, only displays relevant enchants for the character's class and spec currently chosen. For example, when using a Demonology Warlock's Simulationcraft addon output in Top Gear, the enchants listed only pertain to secondary stats and spell damage enchants, omitting enchants that involve healing or non-damage related enchants. The RING section shows options of every type of ring enchant available. The GEMS section allows for a user to choose potential gems to be simulated if their character has any socketed items. By default, the lesser ring enchants and gems are hidden, but can be selected by checking the "Show All Enhancements" option.

All Enhancement windows include a "DEFAULT" and "NONE" button. By clicking these buttons, a user is able to automatically decide which enchants and gems are considered standard and best for maximizing damage. For example, when clicking "DEFAULT" on "MAIN HAND" while simulating a Demonology Warlock, all enchants that provide secondary stat or spell damage are automatically chosen, while healing or utility enchants are not chosen.

###### Talents
The final selection shown is the talent calculator, which allows for considerations of separate talents alongside separate gearsets being simulated. If a user decides to solely simulate gear and their currently equipped talent set, the "TALENT BUILDS TO SIM" section can be ignored, as it selects the currently chosen talents from the character's Simulationcraft addon output. By selecting multiple talents, the number of iterations required will increase, and therefore allow for less gear to be considered. This section is beneficial when considering a small number of talents, but there is a limit on number of iterations allowed to be simulated, which restricts the total number of options to simulate. When a user selects a new talent to be selected, it will become highlighted in an amber color, and add the talent set to the window to the right of the talent calculator, providing a visual of all talent sets being simulated alongside gear and enhancements.

##### How to effectively use Top Gear
The main reason to utilize Top Gear is to decide whether a set of items could lead to a damage output increase. By selecting multiple items in the same slot, alongside currently equipped items, a user is able to determine approximate damage increases or decreases with changing items, while still considering enchants, gems, and talents (whether they're currently selected talents or specific options known to be more or less beneficial with different stats). Ideally, Top Gear is used to compare currently equipped items and talents to new weapons, trinkets, rings, or armor, and the enchants and gems that go along with them. A user is able to select several items to compare all at once (and increases the amount allowed to be simulated when subscribed to Raidbots).

#### Gear Compare
Gear Compare allows for a user to simulate items that a character does not currently possess, unlike Top Gear. Gear Compare is a great option for a user wishing to simulate the hypothetical change if an item were to be obtained and equipped. Gear Compare allows for multiple gearsets to be compared, and can be used with the Simulationcraft addon or through the Armory link.
</br>
*Note: If using the Armory style import, ensure the character has the correct items equipped!*

###### Gearsets
Gear Compare utilizes gearsets in order to compare different hypothetical character simulations. Below the Simulationcraft addon textbox is "COMPARE SETS OF GEAR" immediately followed by "CURRENTLY EQUIPPED" which shows the character's items being worn in-game. The simplest way to utilize Gear Compare is to navigate to the empty gearset, below the "CURRENTLY EQUIPPED" gearset, click "DUPLICATE GEARSET" and then use the "ADD ITEM" to swap any equipped items with hypothetical items, searching for them by name in the search box.

##### How to effectively use Gear Compare
The best use of Gear Compare is typically comparing a character, as is, to a hypothetical gearset with a new item--a weapon, trinket, or piece of Azerite armor, for example. This allows users to see how large of an impact a single item upgrade could be. It is possible to swap multiple items out in a new gearset, though typically used to simulate one major or targeted upgrade, like on-use trinkets or specific weapon(s).

#### Talent Compare
Talent Compare is similar to Gear Compare, but is solely for comparison of talent choices. Talent Compare allows for talent sets to be chosen and simulated against one another when compared to the character's currently chosen talents.

###### Talent Sets
Talent Sets can be chosen in two separate ways: by using the "DUPLICATE TALENT SET" button or the "ADD EMPTY TALENT SET" button. These work almost identically to gearsets from Gear Compare, but the only comparison being made to simulate are talents, and the character's gear is constant throughout every talent set chosen. Talent sets allow for one talent per row to be chosen, but do not require a talent to be chosen in every row. This can allow for quicker selection of damage oriented talents and ignoring of utility based talents.

##### How to effectively use Talent Compare
Talent Compare is a relatively cut-and-dry option to simply decide which talent options are best for the specific encounter style chosen to simulate. The simplest way to create new talent sets is typically to use the "DUPLICATE TALENT SET" button, then change specific talents one by one, creating a comparison of at least two different sets.

#### Quick Sim
Quick Sim allows a user to simulate a character's damage output based on parameters previously mentioned in Simulation Options. There are no options besides the ones covered previously.

##### How to effectively use Quick Sim
A user is able to select the type of encounter, the duration, and number of bosses to be simulated very quickly in Quick Sim. This option is best used for a quick number crunch to determine the potential damage output of a character for a pre-determined fight. This can be helpful when attempting encounters that have damage checks, as players can utilize this method to check their own damage output and consider if the results are satisfactory for the encounter.

#### Stat Weights
Stat Weights allows for a user to simulate the potential damage increase a character could receive if they had 1 additional point of a stat. Stat weights are commonly used to determine what stats are best for a specific character and to determine if an item is an upgrade.

##### How to effectively use Stat Weights
Analyzing Stat Weights can be beneficial to determine the best items to aim for on a character. Stat Weights can be a double-edged sword, though: their weights constantly change. As a character increases in both primary stats, such as intellect or strength, and secondary stats, such as haste or mastery, the weights of every stat changes. Optimally, a user would need to resimulate every time a new piece of gear is obtained. Most classes, though, are able to have a relatively well known stat priority, meaning that there's a typical goal of stats for a character. For example, a Demonology Warlock always wants intellect as their primary stat, and haste will almost always be their best secondary stat, with mastery or critical strike following behind, and versatility being the lowest. These can change, however, based on the amount of each stat held by a character, and leads to the necessity of simulating stat weights frequently enough to ensure a character is using optimal items with proper primary and secondary stats.

#### Advanced
Advanced is typically only used by power users with specific parameters or action priority lists to simulate. For example, a user wishing to simulate a specific length fight with specific add spawning or movement parameters could insert them using the syntax SimulationCraft uses to recreate a known encounter as a simulation option. Unique fights like M.O.T.H.E.R. are a great example, as a character's damage can be largely changed by in-fight events like movement patterns and downtime where a character is unable to attack the boss.

## Understanding Simulation Results
