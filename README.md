# Ansible-Java

An opinionated role that installs Java. Has the ability to configure different versions for the system globally and others for specific users.

Requirements
------------

Requires installation of `json-schema`


### User configuration

User centric version configuration requires that environment variables and path additions be read from `~/.env.d/` 
in a similar fashion as `/etc/profile` parses `/etc/profile.d/`


#### 

```yaml
java:
    - version:		(integer) The version code for the version to install [required]
      vendor:		(enum) Indicates the vendor to install Java from. Currently only supports 'openjdk' [required].
      type:			(enum) Indicates the type of installation. Can be either 'jdk' or 'jre'. Defaults to 'jre'.
      users:		(String array) Users that should have this version configured as their main Java version.
      global:		(boolean) Indicates if this should be set as the global Java version.
```
License
-------

MIT license. See attached license file.

Author Information
------------------

Find me at https://www.hth.is
