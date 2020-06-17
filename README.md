TBC-DB for CMaNGOS/mangos-tbc
======================
A content database for [mangos-tbc][10], and *World of Warcraft Client Patch
2.4.3* - [_Fury of the Sunwell_][50]. It is compatible only with client 2.4.3 (build 8606).

**TBC-DB** is released under the GPL v3.  The file (`LICENSE.md`)
**must** be a part of any redistributable packages made from this software.  No
licenses should be removed from this software if you are making redistributable
copies.

**TBC-DB** contains copyrighted materials that are not part of the GPL v3.
Informations about copyrighted materials are located in the file (`COPYRIGHT.md`).

World of Warcraft content and materials are trademarks and copyrights of Blizzard or its licensors. All rights reserved.
**TBC-DB** is part of CMaNGOS project and is not affiliated with Blizzard or its licensors.

Compatibility
-------------
The *TBC-DB* database is compatible with [mangos-tbc][10] core only.

Getting started
---------------
The basic principle behind this database repository is to have a single SQL file
holding every table in the database. When something is changed into the database
the modification is done by adding small SQL update files placed into the `updates` directory.
Every time a user (that would be you or TBC-DB Developers) wishes to change something into the database, he/she
have to create and add the right SQL file. This helps tracking what changes are made, when and where.

Installation
------------
**TBC-DB** is the main content database for: `tbcmangos` where the world is defined
with creatures, items, objects, quests, etc.

It must be applied after creating the `tbcmangos` database from your CMaNGOS core distribution [mangos-tbc][10] from [CMaNGOS Project][13].

If you used the default values when installing your mangos core, simply run into a bash compatible shell (like Bash Git for Windows) the following command `./InstallFullDB.sh`.

It will create a single file InstallFullDB.config .

If you have modified the default values for connecting to the database, in order to use this database repository, you will have to open `InstallFullDB.config`, and edit in the desired database, username and password according to how you have configured your MySQL server. Default values for mangos core are `username:mangos`, `password:mangos`, `database:mangos`. For security reasons, it is strongly adviced to use different username and password.

Once you have the desired database user and rights configured in MySQL, you may run again the `./InstallFullDB.sh` command to load the individual data tables into your database, populate them and apply all updates since the last milestone.

For a full installation guide, please refer to [CMaNGOS installation instructions][14].

Contributing
------------
You are welcome to contribute to this database project. There are three main ways of contributing. Choose the one fitting your skills.

1. Open a ticket/issue on [CMaNGOS issue tracker][15] on GitHub. Describe the issue as accurately as
possible, how things currently are, how things should be instead. Example: "NPC Mighty Skeleton in Western Plaguelands does not wield its weapon. It should have a sword.". You can improve your issue report by giving the ID/entry of the creature, object, quest, spell... it helps developers to find quickly where is the problem. In-game GM commands like `.guid`, `.lookup quest (or creature, spell, object)`, `.gobject near (or target)` are great to get those informations
2. If you have SQL knowledge you can also open a ticket/issue and provide a fix, even partial. To help you to understand the DB structure, have a look a the [wiki page][16] or feel free to ask developers in the issue report. You can also try to fix currently open issues
3. Make a pull request. If you feel like [cloning the database repository][17], you can test your own fixes and [do a pull request][18] that will be reviewed and discussed with you before merging

Whenever possible, provide sources about the issue to help developers to get a better understanding of the issue (wowwiki, wowpedia, wowhead, official data...). Note that everything coming from private servers *is not* a reliable source.

Note that the more complete your contribution is (i.e. close to a pull request), the quicker it will become part of the database.
But as this is a community project, the developers will always try to help you move through the various stages of contributing!

[1]: https://github.com/cmangos/mangos-tbc "mangos-tbc"

[10]: https://github.com/cmangos/mangos-tbc/ "mangos tbc"
[12]: https://github.com/cmangos/tbc-db/ "content database"
[13]: http://www.cmangos.net/ "CMaNGOS Project"
[14]: https://github.com/cmangos/issues/wiki/Installation-Instructions "CMaNGOS installation instructions"
[15]: https://github.com/cmangos/issues/issues/ "CMaNGOS issue tracker"
[16]: https://github.com/cmangos/issues/wiki/mangosdb_struct
[17]: https://help.github.com/articles/fork-a-repo/
[18]: https://help.github.com/articles/creating-a-pull-request/

[50]: http://eu.blizzard.com/en-gb/games/wow/ "World of Warcraft"
[51]: http://www.wowpedia.org/Patch_2.4.3 "WoW 2.4.3 - Fury of the Sunwell"

[101]: http://github.com/ "github - social coding"
