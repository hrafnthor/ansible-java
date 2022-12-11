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

`java_architecture`: [String] Used for defining the openjdk installation folder. 

- Accepted values are `"amd64"`

`java_vendor`: [String] Indicates the Java vendor to install from

- Accepted values are `"openjdk"`

`java_type`: [String] Indicates the package type to install

- Accepted values are `"jdk", "jre"`

`java_version`: [Integer] Indicates the version to install

- Accepted values are `8, 11, 17, 18, 19`

`java_global`: [Boolean] Indicates if the installation should be configured globally. 

- If `true` then the given `java_version` will be set at the default `java` implementation on the system level

- If `false` then the given `java_version` will be configured specifically for the user defined by the now required `java_user` variable

`java_user`: [String] The username for which whom the given `java_version` will be configured specifically.

- Will only be used if `java_global` is set to `false`


License
-------

MIT license. See attached license file.

Author Information
------------------

Find me at https://www.hth.is
