# Nest Watcher
A Program to analyze nests in your area, save it to a database and send Discord notifications about them.

## Links
- [Discord](https://discord.gg/q6MSBg4ugv) for help and keeping up with changes
- [Wiki](https://ccev.github.io/nestwatcher/) to get everything running

# additional Informations to this Version
- Clone repository `git clone https://github.com/ReuschelCGN/nestwatcher`
- Copy content of `docker-compose.yml` into your running `docker-compose.yml`
- Rename folder `config_example` to `config` and fill out the files (look here for more Info: [Wiki](https://ccev.github.io/nestwatcher/)):
   - `areas.json`
   - `config.ini` 
(config.ini in this Version only works with UIcon Repos for `icon_repo` and also on Tileserver Template)
   - `discord.json`
   - `settings.json` 
- Add NestWatcher Template `nests.json` to your Tileserver.
- Add NestWatcher DB Table from SQL Folder to your DB (nests.sql & -> update.sql)
- then run:
   - `docker-compose build nestwatcher`
   - `docker-compose up -d nestwatcher`
- and for edit nestnames:
   - `docker exec -it nestwatcher /bin/sh`
   - `python3 tools.py`
([Wiki-Nestnames](https://ccev.github.io/nestwatcher/tools/renaming-nests.html)
