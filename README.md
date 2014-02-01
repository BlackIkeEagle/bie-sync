Documents sync
==============

Simple way to sync your 'Documents' from and to a central storage

documents-sync usage
--------------------

```sh
$ documents-sync up
```

Sync to the 'master' server, will dry-run with the above command so the output will be what files will be updated when the command is actually 'run'.

```sh
$ documents-sync up run
```

Run the actual sync.

```sh
$ documents-sync down
$ documents-sync down run
```

Same principle as for up :).

documents-sync.cfg
------------------

By default you have to put the configuration file in: `~/.config/documents-sync/documents-sync.cfg`

There are 4 options you can set in the config file:

```
LFOLDER="/path/to/local/folder"
RFOLDER="/path/to/remote/folder"
DOCUMENTS="Documents"
SSH=0
```

When you want to sync over ssh change RFOLDER and SSH:

```
LFOLDER="/path/to/local/folder"
RFOLDER="server:/path/to/remote/folder"
DOCUMENTS="Documents"
SSH=1
```

documents-sync.exclude
----------------------

Exclude some files from the sync. The file can be found in `~/.config/documents-sync/documents-sync.exclude`.
Just add exclude entries as described in the rsync manual.
