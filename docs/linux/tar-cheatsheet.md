---
title: 'Tar Cheatsheet'
tags: ['linux','shell','tar','cheatsheet']
---
# Tar Cheatsheet
## Parameters

| Option | Description                                                                                                                                          |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| -c     | Creates a new archive                                                                                                                                |
| -f     | Writes archive to a file, or extracts from a file.  This option always has to be entered last, since all subsequent entries are interpreted as files |
| -x     | Extracts files from the archive. The files remain in the archive                                                                                     |
| -t     | Displays a list of files in the archive                                                                                                              |
| -k     | Prevents files from being overwritten when extracting an archive                                                                                     |
| -p     | Maintains access rights when extracting an archive                                                                                                   |
| -v     | Increases verbosity                                                                                                                                  |
| -C     | Changes to a directory before creating / extracting an archive                                                                                       |
| -z     | Use gzip compression when creating / extracting an archive                                                                                           |
| -j     | Use bzip2 compression when creating / extracting an archive                                                                                          |
| -J     | Use xz compression when creating / extracting an archive                                                                                             |

## Creating an archive with gzip compression (full paths in archive)

```shell
tar -cvzpf ~/my-archive.tar.gz /path/to/dir-to-archive
```

## Same as above, but switch to directory before creating archive (relative paths in archive):

```shell
tar -cvzpf ~/my-archive.tar.gz -C /path/to/dir-to-archive .
```