---
title: Changelog
---

This is an incomplete list compiled for convenience, see pull requests for all changes.

Starts with
[revision 10614 (just before pockets)](https://github.com/cataclysmbnteam/Cataclysm-BN/commit/8cea0fce70c87ea93c6fd4e409c68558e24ce42e)
of [CleverRaven/Cataclysm-DDA.](https://github.com/CleverRaven/Cataclysm-DDA)

## Stable v 0.3

### Gameplay

- New scenario: Play as Feral and befriend with zombies (on certain conditions).
- Added ability to manually connect and disconnect multiple power grids via voltmeter and some
  materials.
- Added shields to the game.
- Further improvements to Rule of Cool explosions:
  - Chain explosions.
  - Items turn into shrapnel.
  - Custom animations.

### Balance

- Improved mechs.
- Added craftable helicopter rotors.
- Water cannons can now fire acid.
- Buffed water purification methods.
- Yet more tweaks to bows (decreased damage, strength cap is now a soft cap).
- Tweaked power armor spawn locations.

### New content

- Added new CBMs. Some CBMs ported from existing mods.
- A lot of locations reworked and improved.
- Expansion to the Old Guard faction.

### Infrastructure

- Lab Finale rework.
- Updates to build files.
- Weapon categories for martial arts and gunmods (eases mod integrations).
- Allow NPCs to use all bionic weapons not just the hardcoded list.
- Improve code for NPC method of attack, generally improving their ability to choose weapons and
  attacks. Allows them to reload magazines and perform combat reloads with single shot weapons.

### Bugfixes

- Multiple bugfixes related to NPC AI weapon selection and ranged attacks.
- Fixes to off-road vehicle behavior.
- Fix to the long-standing issue when not all overmap specials could spawn if there were too many
  mods enabled.
- Fixes to monster attacks and movement over z-levels.

### Ported from later versions of DDA

- Feral humans (with additional tweaks).
- Additional achievements.

## Stable v 0.2

### Gameplay

- Rework teleglow, nether attention, stare monattack.
- AI now can target and shoot moving cars.
- Food items now show how temperature affects it rot.
- Graphical overmap now enabled by default. Obsolete Graphical Overmap mod, rename to Larwick's
  Overmap.
- Reorganized mod resources. All Bright Nights resources now labeled with unique id.
- Allows pushing vehicles over ramps.
- Melee skill actually impacts attack stamina usage.
- Add the ability to mark items as favorite from the multidrop menu.

### Balance

- Finished ammo and armor rebalance. Armour piercing ammunition now more effective agaisnt armored
  targets, but armor in certain cases provides somewhat better protection against gunshots. Changes
  included reworked power armor stats.
- remove glare protection requirement for forged frames.
- Make bicycle alternators (dynamos) craftable.
- Allow repairing items with forges.
- Allow easier installing/removing of some parts.
- Robots no longer completely immune to lasers.
- Prevents dodge gain exploit.
- Wraith and shadow special attack updates.
- Shadow and cult creature updates from Arcana.
- Adjustments to mi-go locations, atmosphere field.

### Quality of Life

- Added ability Submit bug report directly from game.
- Reduce blinking effects speed (300 -> 800ms), and add an option to change it in game.
- Deactivate pet robots in pet menu instead of query.
- While flying, warn when letting go of control or stop driving.

### Infrastructure

- Migrate to C++17.
- Implement relic recharge.
- Grid constructions now use workshop category.
- Allow marking construction recipes as favorite, sort recipes by name in construction UI.

### New Content

- Added new electric grid appliances.
- Adds grid forge rigs, chemistry sets, and chemlabs.
- Added hauler bot.
- Most of the building contains built in electric grids.
- Add grid flag to more specials, mods in particular.
- Added new helicopter parts group to helipad.
- Add mountable autodoc and autodoc couch.

### Ported from later versions of DDA

- Port complete leash and lead system.
- Port over fix for spellcasting monsters and summon spells.
- Updated DinoMod.
- Add in-game progression diary.
- Cathedral overhaul.
- add NPCs to biker_dump.
- Port Barbaran Montante and rebalance.

### Other

- Add missing damage sources kills and suicide to kills list.

## Stable v 0.1

### Gameplay

- Victory condition: <details><summary>spoilers</summary>Somewhere in the rectangular region of the
  overmap from (0'0, 0'0) to (0'179, 0'179), there's a central lab (accessible from a tile named
  "access shaft" on z = -1) that has a red-colored "L" tile at its bottom z-level. Find the lab,
  reach the bottom, then either sacrifice your own life or put in a mininuke.</details>
- (Currently WIP, but already functional) Electric grid system, without use of vehicles, but able to
  connect to them. See
  [Electric Grids page](https://github.com/cataclysmbnteam/Cataclysm-BN/wiki/Electric-grids) for
  more info.
- Lower height levels (z-levels) drawn.
- Angled vehicles don't develop "holes" in their normally-impenetrable walls. This affects all
  relevant game mechanics such as monster and player movement, line of sight calculation, light and
  scent propagation, etc.
- Reworked helicopters:
  - Every character/profession can use helicopters
  - It is possible to build helicopters, if you scavenge the blades from an existing one
  - Reduced helicopters fuel consumption to allow flying for ingame hours
  - Rotors no longer break from collisions
  - Atomic Helicopter exist
- Ranged in general:
  - Burst fire reworked: all shots fired at same accuracy, with recoil-dependent penalty to all of
    them. Penalty is of same magnitude as dispersion for most guns and can be 0 for lighter ones
  - Headshots downgraded to crits with 150% damage (from >200%), grazing shots upgraded to 50% (was
    0%-25%)
  - Some shotgun ammunition provides cone-shaped aoe attack
- Bows and crossbows:
  - Stats buffed (crossbows much more than bows)
  - Crossbows easier to craft
  - Removed special cases dependent on target hp
- Buffed drugs roughly back to their pre-nerf stats
  - Except meth, this one provides a long term (12h), weak (5 speed, 1 per) buff and prevents
    sleepiness
  - Morale boosts from drugs last as long as drug effects themselves
- Grabs:
  - Grab and pain penalties stack less
  - Physically damaging a grabbing enemy will often break the grab (100% chance for hits taking at
    least 10% of max hp)
  - Grabs don't affect blocking and affect dodging much less
  - Grab attacks are faster and followed up by a free regular attack on hit
- AoE attacks (from axes, spears and lajatangs) lose their requirements
- Winded condition removed
- Explosives rebalanced: lower ranges, blast damage rounded to 100%/50%/0%, shrapnel hits exactly
  once for damage not dependent on distance
  - "Rule Of Cool explosions" debug setting: explosions damage only terrain and creatures in their
    line of sight, so hiding behind a corner actually works now
- Explosives, wheels and bullets no longer damage items. Strong enough explosions can still destroy
  them, and all 3 will pulp corpses that can revive.
- Fires stack less, makes flamethrowers less damaging to player character
- Mutations:
  - Trait costs rebalanced to reflect their actual impact better
  - Combat mutations (armor, claws) improved
  - Some "free points" traits removed from character generation (heavy sleeper, bad liar etc.)
  - Undirected mutations happen in bulk, their number based on time since last mutation.
  - Mutations tend towards "somewhat better than at start" point-wise, to compensate for the fact
    that most bad mutations are more bad than most good mutations are good
  - Mutant toxins redesigned: will cause mutations once accumulated high enough, but cause no
    penalties
- CBM installation is now guaranteed, but after that failure effects may still appear. So even
  failed operation gives bionic to player in workable condition. CBM uninstallation still can fail
  completely. Autodoc can't instantly kill the player due to operation failure - instead of doing
  fatal damage player will be infected. Damage to player body during operation failures is now
  affected by bionic installation difficulty.
- Turrets return fire against silent attackers, but not against attackers outside range. Also the
  code respects turrets' stats and skills better now.
- Surgery trains first aid, scaling with target size and number of possible bionics.
- Food:
  - Remove obesity mechanics and most of stomach mechanics
  - Starvation death now takes a week from fully fed
  - Removed slower hunger/thirst during sleep
- Removed animal waste product mechanics
- Removed tetanus, random cold and flu
- Fungal spores no longer spawn fungaloids, fungal disease doesn't break arms
- Reworked food temerature mechanics. Removed "mushy" mechanics. Rot still affected by temperature.
  Note that freezers still work as intended and prevent rot, and fire makes you warm.

### Quality of life

- Crafting defaults to in inventory/on the ground, best workbench in radius is used anyway
- Can read items on the floor, in vehicles etc. Reading doesn't automatically pick up books, but
  leaves them on the spot.
- Crafting in progress displays time left and crafting modifiers
- Butchery uses tools in crafting radius, warns about problems
- Deployable butchery furniture doesn't require deployment, works in item form
- Unloading no longer moves the item to inventory if it wasn't there before
- Can move items up and down z-levels in AIM (Advanced Inventory Management)
- Target list (during shooting and reach attacks) allows shooting through windows and above vehicles
  (from a turret)
- Sight range of at least 1 tile is guaranteed when not blind
- Tile memory does not decay
- Added accurate firearm dispersion/recoil stats that include all the modifiers (from skill,
  bionics, encumbrance and so on)

### New content

- Medical zombie tree, focused on debuffing
- New automated gun turrets replacing CROWS based ones. Less deadly, but don't drop tons of valuable
  rifle ammo.
- Bionic scanner, to detect which corpses are worth cutting up

### Performance

- Fires do not produce hot air and smoke, no longer affected by wind
- Option to disable event bus system (in Debug tab) - removes one big cycle hog, but also
  achievements and statistics
- Food isn't affected by radiant heat or hot air
- Removed slow fd_clairvoyant check which only benefited Magiclysm, but slowed down everyone
- Cache list of all vehicles on map, since getting it is slow in 3D mode

### Ported from later versions of DDA

- Ground vehicle z-level transitions and z+1 bridges. Ramps can be enabled through "Z-levels" world
  setting, new bridge generation - through "Elevated bridges" mod.
- Graphical overmap drawn with SDL using sprites.
- Improved autodrive.
- Various under-the-hood improvements, such as refactors and optimizations.
- Hundreds of bugfixes and small changes.

### Other

- 3rd party mods translation support
- UnDeadPeople tileset included
- Restored atomic cars
- Restored MBR vests (with some rebalance). ESAPI vest removed
