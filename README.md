Role Name
=========

An opinionated role that installs Java. Has the ability to configure different version on the system level than for a specific user.

Requirements
------------

No external requirements.

User centric version configuration requires that environment variables and path additions be read from ~/.profile.d/ 
in a similar fashion as /etc/profile parses /etc/profile.d/


Role Variables
--------------

`java_architecture` : [string] (required) Used for defining the openjdk installation folder. 

- Accepted values are `"amd64"`

`java_vendor` : [string] (required) Indicates the Java vendor to install from

- Accepted values are `"openjdk"`

`java_type` : [string] (required) Indicates the package type to install

- Accepted values are `"jdk", "jre"`

`java_version` : [integer] (required) Indicates the version to install

- Accepted values are `8, 11, 17, 18, 19`

`java_global` : [boolean] (optional) Indicates if the installation should be configured globally (default: true).

`java_users` : [list] (optional) Contains the usernames that will have the requested Java version configured as their default, overriding any system level value.


License
-------

MIT license. See attached license file.

Author Information
------------------

Find me at https://www.hth.is
