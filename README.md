# propel-versionable
Propel Versionable behavior, fixed version.

There is a bug in original Versionable behavior in Propel1: https://github.com/propelorm/Propel/pull/693 . Propel generates
incorrect PHP and SQL files in some cases. The pull request has not been accepted yet, that's why I had to create my own fixed
version.

The fixed version uses the original code and this pull request as a fix + unit tests: https://github.com/propelorm/Propel/pull/778


Installation
------------
Using Composer:

```json
{
    "require": {
        "crzdeveloper/propel-versionable": "1.*"
    }
}
```

Then register behavior in either your ```propel.ini``` or ```buid.properties```
configuration file:

``` ini
propel.behavior.versionable.class = <path to crzdeveloper/propel-versionable>
```

Or in case you use composer:
``` ini
propel.behavior.versionable.class = \Crzd\Proppel1\Behavior\Versionable\VersionableBehavior 
```