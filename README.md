Bie sync
========

Simple way to sync your folders from and to a central storage

bie-sync usage
---------

```sh
$ bie-sync [options] profile
```

Sync to the 'master' server, will dry-run with the above command so the output will be what files will be updated when the command is actually 'run'.

```sh
$ bie-sync --up --run profile
```

Run the actual sync.

profile.cfg
------------------

By default you have to put a configuration file in: `~/.config/bie-sync/profile.cfg`

There are 3 options you can set in the config file:

```
LFOLDER="/path/to/local/folder"
RFOLDER="/path/to/remote/folder"
SSH=0
```

When you want to sync over ssh change RFOLDER and SSH:

```
LFOLDER="/path/to/local/folder"
RFOLDER="server:/path/to/remote/folder"
SSH=1
```

profile.exclude
----------------------

Exclude some files from the sync. The file can be found in `~/.config/documents-sync/profile.exclude`.
Just add exclude entries as described in the rsync manual.
