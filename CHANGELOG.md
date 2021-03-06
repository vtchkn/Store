Change Log
==========

The change log for Store version 1.x can be found [here](https://github.com/NYTimes/Store/blob/develop/CHANGELOG.md).

Version 3.0.0-alpha *(2017-05-23)*
----------------------------

This is a first alpha release of Store ported to RxJava 2.

**New Features**

* (#155) Port to RxJava 2
* (#220) Packages have been renamed to store3 to allow use of this artifact alongside the original Store
* (#185) Return Single/Maybe where appropriate
* (#189) Add lambdas to Store and Filesystem modules
* (#214) expireAfterAccess added to MemoryPolicy
* (#214) Deprecate setExpireAfter and getExpireAfter -- use new expireAfterWrite or expireAfterAccess, see #199 for 
MemoryPolicy changes
* (#214) Add Raw to BufferedSource transformer


**Bug Fixes and Stability Improvements**

* (#214) Fix networkBeforeStale on cold start with no connectivity
* (#214) Add a missing source.close() call
* (#164) FileSystemPersister.persisterIsStale() should return false if record is missing or policy is unspecified
* (#166) Remove apt dependency and use annotationProcessor instead
* (#214) Standardize store.stream() to emit only new items
* (#214) Fix typos
* (#214) Close source after write to filesystem