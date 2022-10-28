---
title: 'Group Types & Entities'
sidebar_position: 1
---

# Group Types & Entities

<br />

### `(Enum)` Group Role

```bash
'achiever', 'adamant', 'adept', 'administrator', 'admiral', 'adventurer', 'air', 'anchor', 'apothecary', 'archer', 'armadylean', 'artillery', 'artisan', 'asgarnian', 'assassin', 'assistant', 'astral', 'athlete', 'attacker', 'bandit', 'bandosian', 'barbarian', 'battlemage', 'beast', 'berserker', 'blisterwood', 'blood', 'blue', 'bob', 'body', 'brassican', 'brawler', 'brigadier', 'brigand', 'bronze', 'bruiser', 'bulwark', 'burglar', 'burnt', 'cadet', 'captain', 'carry', 'champion', 'chaos', 'cleric', 'collector', 'colonel', 'commander', 'competitor', 'completionist', 'constructor', 'cook', 'coordinator', 'corporal', 'cosmic', 'councillor', 'crafter', 'crew', 'crusader', 'cutpurse', 'death', 'defender', 'defiler', 'deputy_owner', 'destroyer', 'diamond', 'diseased', 'doctor', 'dogsbody', 'dragon', 'dragonstone', 'druid', 'duellist', 'earth', 'elite', 'emerald', 'enforcer', 'epic', 'executive', 'expert', 'explorer', 'farmer', 'feeder', 'fighter', 'fire', 'firemaker', 'firestarter', 'fisher', 'fletcher', 'forager', 'fremennik', 'gamer', 'gatherer', 'general', 'gnome_child', 'gnome_elder', 'goblin', 'gold', 'goon', 'green', 'grey', 'guardian', 'guthixian', 'harpoon', 'healer', 'hellcat', 'helper', 'herbologist', 'hero', 'holy', 'hoarder', 'hunter', 'ignitor', 'illusionist', 'imp', 'infantry', 'inquisitor', 'iron', 'jade', 'justiciar', 'kandarin', 'karamjan', 'kharidian', 'kitten', 'knight', 'labourer', 'law', 'leader', 'learner', 'legacy', 'legend', 'legionnaire', 'lieutenant', 'looter', 'lumberjack', 'magic', 'magician', 'major', 'maple', 'marshal', 'master', 'maxed', 'mediator', 'medic', 'mentor', 'member', 'merchant', 'mind', 'miner', 'minion', 'misthalinian', 'mithril', 'moderator', 'monarch', 'morytanian', 'mystic', 'myth', 'natural', 'nature', 'necromancer', 'ninja', 'noble', 'novice', 'nurse', 'oak', 'officer', 'onyx', 'opal', 'oracle', 'orange', 'owner', 'page', 'paladin', 'pawn', 'pilgrim', 'pine', 'pink', 'prefect', 'priest', 'private', 'prodigy', 'proselyte', 'prospector', 'protector', 'pure', 'purple', 'pyromancer', 'quester', 'racer', 'raider', 'ranger', 'record_chaser', 'recruit', 'recruiter', 'red_topaz', 'red', 'rogue', 'ruby', 'rune', 'runecrafter', 'sage', 'sapphire', 'saradominist', 'saviour', 'scavenger', 'scholar', 'scourge', 'scout', 'scribe', 'seer', 'senator', 'sentry', 'serenist', 'sergeant', 'shaman', 'sheriff', 'short_green_guy', 'skiller', 'skulled', 'slayer', 'smiter', 'smith', 'smuggler', 'sniper', 'soul', 'specialist', 'speed_runner', 'spellcaster', 'squire', 'staff', 'steel', 'strider', 'striker', 'summoner', 'superior', 'supervisor', 'teacher', 'templar', 'therapist', 'thief', 'tirannian', 'trialist', 'trickster', 'tzkal', 'tztok', 'unholy', 'vagrant', 'vanguard', 'walker', 'wanderer', 'warden', 'warlock', 'warrior', 'water', 'wild', 'willow', 'wily', 'wintumber', 'witch', 'wizard', 'worker', 'wrath', 'xerician', 'yellow', 'yew', 'zamorakian', 'zarosian', 'zealot', 'zenyte'
```

<br />

### `(Object)` Group

| Field       | Type    | Description                              |
| :---------- | :------ | :--------------------------------------- |
| id          | integer | The group's ID.                          |
| name        | string  | The group's name.                        |
| clanChat    | string  | The group's clan chat (1-12 characters). |
| description | string? | The group's description.                 |
| homeworld   | number? | The group's homeworld.                   |
| verified    | boolean | The group's verified status.             |
| score       | integer | The group's global ranking score.        |
| createdAt   | date    | The group's creation date.               |
| updatedAt   | date    | The group's last modification date.      |
| memberCount | integer | The group's total number of members.     |

<br />

### `(Object)` Membership

| Field     | Type                                                             | Description                                                      |
| :-------- | :--------------------------------------------------------------- | :--------------------------------------------------------------- |
| playerId  | integer                                                          | The player's ID.                                                 |
| groupId   | integer                                                          | The group's ID.                                                  |
| role      | [GroupRole](/groups-api/group-type-definitions#enum-group-role)? | The player's role (rank) in the group.                           |
| createdAt | date                                                             | The date at which the player was added as a member to the group. |
| updatedAt | date                                                             | The date at which the membership was updated.                    |

<br />

### `(Object)` Group Membership

Returned in group-centric endpoints.

> extends [Membership](/groups-api/group-type-definitions#object-membership)

| Field  | Type                                                         | Description              |
| :----- | :----------------------------------------------------------- | :----------------------- |
| player | [Player](/players-api/player-type-definitions#object-player) | The membership's player. |

<br />

### `(Object)` Player Membership

Returned in player-centric endpoints.

> extends [Membership](/groups-api/group-type-definitions#object-membership)

| Field | Type                                                     | Description                          |
| :---- | :------------------------------------------------------- | :----------------------------------- |
| group | [Group](/groups-api/group-type-definitions#object-group) | The group the player is a member in. |

<br />