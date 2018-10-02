0.15.0
======

 - depend on filelock library to avoid locking bug
   ([#89](https://github.com/acid-state/acid-state/issues/89))
 - permit events that are polymorphic in the base monad, with a MonadReader/MonadState constraint
   ([#94]((https://github.com/acid-state/acid-state/pull/56)))
 - add a test suite and extend examples
   ([#98](https://github.com/acid-state/acid-state/pull/98))
 - fix a minor memory leak
   ([#104](https://github.com/acid-state/acid-state/pull/104))
 - expose internal modules (subject to change in the future)

0.14.3
======

 - support building on GHC 8.2
 - update links from seize.it to github.com

0.14.2
======

 - createCheckpoint now cuts a new events file (bug #74)

0.14.1
======

 - fix bug in archiveLog that resulted in logs being moved prematurely (bug #22)
 - tweaks for GHC 8.0.x, template-haskell 2.11.x
 - fix compilation of benchmarks

0.14.0
======

 - fixes for cereal 0.5 while maintaining cereal 0.4
   compatibility. IMPORTANT: cereal 0.5 / safecopy 0.9 change the
   serialization format of Float/Double. Migration should be performed
   automatically on old data. However, you should be aware that once
   you upgrade to safecopy 0.9 / cereal 0.5, your data will be
   migrated and not readable by older versions of your application
   which are compiled against safecopy 0.8 / cereal 0.4.

 - additional fixes for TH and kinded type variables
   [https://github.com/acid-state/acid-state/pull/56](https://github.com/acid-state/acid-state/pull/56)
