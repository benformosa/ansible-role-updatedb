## updatedb

[![CI](https://github.com/benformosa/ansible-role-updatedb/workflows/CI/badge.svg)](https://github.com/benformosa/ansible-role-updatedb/actions?query=workflow%3ACI)
[![Ansible Role](https://img.shields.io/ansible/role/54030.svg)](https://galaxy.ansible.com/benformosa/updatedb)
[![GitHub release](https://img.shields.io/github/v/release/benformosa/ansible-role-updatedb.svg)](https://github.com/benformosa/ansible-role-updatedb/releases/latest)


Manage updatedb Debian-like systems.

Forked from [Oefenweb/ansible-updatedb](https://github.com/Oefenweb/ansible-updatedb) to add RHEL support.

#### Requirements

* `mlocate` (will be installed)

#### Variables

 * `updatedb_prune_bind_mounts` [default: `true`]: Whether or not bind mounts are scanned
 * `updatedb_prunenames` [default: `[]`]: A list of directory names (without paths) which should not be scanned (e.g. `.git`, `.bzr`, `.hg`, `.svn`)
 * `updatedb_prunepaths` [default: `[/tmp, /var/spool, /media, /home/.ecryptfs]`]: A list of path names of directories which should not be scanned
 * `updatedb_prunefs` [default: `[NFS, nfs, nfs4, rpc_pipefs, afs, binfmt_misc, proc, smbfs, autofs, iso9660, ncpfs, coda, devpts, ftpfs, devfs, mfs, shfs, sysfs, cifs, lustre_lite, tmpfs, usbfs, udf, fuse.glusterfs, fuse.sshfs, curlftpfs, ecryptfs, fusesmb, devtmpfs]`]: A list of file system types (as used in /etc/mtab) which should not be scanned

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - updatedb
```

#### License

MIT

#### Author Information

* Mischa ter Smitten
* Ben Formosa

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/benformosa/ansible-role-updatedb/issues)!
