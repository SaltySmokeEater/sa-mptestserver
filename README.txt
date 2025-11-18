NG-RP Server Skeleton
=====================

This is a skeleton folder for running the NG-RP SA-MP gamemode locally.
It contains placeholder files and a ready-to-edit server.cfg aimed at local MariaDB hosting.

Important next steps:
1. Replace the placeholder files (ngrp.amx, libmariadb.dll, streamer.dll, etc.) with the real files from the NG-RP repo and required plugins.
2. Import 'ngrp.sql' into your local MariaDB:
   mysql -u root -p ngrp < ngrp.sql
3. Edit server.cfg:
   - Set mysql_user and mysql_pass to real credentials.
   - Ensure 'plugins' line matches the actual plugin filenames you install.
4. Put samp-server.exe in the root of this folder (or use the provided binary if you have one).
5. Start MariaDB and test with:
   mysql -h 127.0.0.1 -P 3306 -u root -p

Folder layout summary:
- gamemodes/: contains the gamemode .amx (compiled) and .pwn (source)
- plugins/: put all plugin DLLs here (streamer, mysql/libmariadb, sscanf, crashdetect, etc.)
- scriptfiles/: game data (houses, vehicles, logs)
- pawno/: compiler + include files (optional)
- ngrp.sql: game schema to import into the DB

Note: This skeleton intentionally uses placeholder binaries (zero-length files) for licensing reasons.
Replace them with the official binaries downloaded from the NG-RP repo and SA-MP plugin pages.
