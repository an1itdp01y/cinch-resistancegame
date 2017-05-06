# Oberon/Assassin can kill himself but should not be able to

(Since `!assassin_is_oberon`) would be false.

# In Lancelot games, display Lancelot status in !missionN, !missions

MISSION 3 can become MISSION 3 - Lancelots original
for !missions, unclear how to make it compact enough.

# Trapper result should not highlight

X and Y should dehighlight X and Y.

Same with X xCals Y in excalibur result.

# In Lancelot #3, Spies should not know which spy is Evil Lancelot.

# Lancelot warnings leak information to otherwise-blind spies

`warn_about_lancelots` warns spies of a Lancelot switch and names specifically which player is Evil lancelot. This information is (correctly) not revealed to Oberon. It should also not be revealed to Spy Rogue or Blind Spy Reverser

# Don't reveal Trapper result until Excalibur target is chosen

http://boardgamegeek.com/thread/1287793/trapper-and-sergeantexcalibur-which-happens-first

Don E's official ruling is that it should be "Leader pick, Sergeant pick, both look". We currently implement "Leader pick and look, Sergeant pick and look".

# Cumulatively show all mission results

Instead of
PASS
(wait 3 seconds)
PASS
(wait 3 seconds)
FAIL

What about:
PASS
(wait 3 seconds)
PASS PASS
(wait 3 seconds)
PASS PASS FAIL

More readable in the face of people yelling PASS or FAIL randomly (yes I know that's a social problem, but hell I think it's useful to have in either case!!!)

# `get_game_settings` on a base game shows no roles

Reversers and Rogues mean that base games can have roles too. Should show them.

https://github.com/caitlin/cinch-resistancegame/blob/master/lib/cinch/plugins/resistance_game.rb#L1432

# Excalibur and reversers/rogues/spy chiefs

Either need to be implemented (currently we only do pass<->fail), or we should refuse to start a game mixing excalibur and any of these roles.

Current behavior is: excaliburing a rogue-success or reverse does nothing to that card (which I absolutely feel justified in calling a bug).

chief fail is not implemented yet so we don't need to worry about it yet
