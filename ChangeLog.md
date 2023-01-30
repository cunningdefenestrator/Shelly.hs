# 1.12.0

Cunning Defenstrator, 2023-01-29
* Rework ShellCmd's instances to support String arguments.
* Add some tests.
* Remove the IncoherentInstances pragma as it's deprecated.
* Bump the major version as CmdArg's method has changed.  Users must migrate
  existing instances by replacing `toTextArg` with `toTextArgs` and wrapping the
  old return value in a list.
* Bump the resolver to lts-20.04 (the latest as of this writing).
* Bump haskell-ci to 0.15.20230128

# 1.11.0

Andreas Abel, 2023-01-24
* Restore running of local scripts, e.g. `cmd "./foo.sh"`:
  Issue [#107](https://github.com/gregwebs/Shelly.hs/issues/107)
  fixed by Alfredo di Napoli in PR
  [#216](https://github.com/gregwebs/Shelly.hs/pull/216).
* Builds with GHC 8.0 - 9.4.

# 1.10.0.1

Andreas Abel, 2023-01-24
* Allow `unix-compat-0.6`.
* Builds `-Wall` warning-free with GHC 8.0 - 9.4.

# 1.10.0

Andreas Abel, 2022-01-30
* Allow `transformers-0.6`:
  - Replace `ErrorT` by `ExceptT`.
  - Remove `MonadSh` and `MonadShControl` instance for `ListT`.
    [#211](https://github.com/gregwebs/Shelly.hs/pull/211)
* Bump lower bounds of dependencies, keeping all versions that build with GHC >= 8.0.
* Remove unused `unix` dependency.
* Allow `time-1.12`.
* Builds warning-free with GHC 8.0 - 9.2.1.

# 1.9.0

Greg Weber, 2019-08-29
* Drop dependencies `system-fileio` and `system-filepath` in favor of `filepath`:
  The `FilePath` type changed to a synonym of `String`.
* Allow `time >= 1.9`.
* Builds with GHC >= 8.0 (tested up to 9.2).

# 1.8.1

Greg Weber, 2018-05-30
* New function `cp_should_follow_symlinks` to specify whether a copy should follow symlinks.

# 1.8.0

Greg Weber, 2018-05-09
* `cp_r` now uses upper case R: `cp -R`.

# 1.7.2

Greg Weber, 2018-03-17
* Fix handling of case-insensitive environment variables on Windows.
  [#166](https://github.com/yesodweb/Shelly.hs/issues/166)

# 1.7.1

Greg Weber, 2018-03-06
* Support `exceptions-0.9`.

# 1.7.0.1

Greg Weber, 2018-01-23
* Fix `FindSpec.hs` tests.
  Fixes [#150](https://github.com/yesodweb/Shelly.hs/issues/150)
  and [#162](https://github.com/yesodweb/Shelly.hs/issues/162).

# 1.7.0

Greg Weber, 2017-12-10
* Quote `ssh` remote commands aggressively with single quotes.
  [#160](https://github.com/yesodweb/Shelly.hs/issues/160)

# 1.6.9

Greg Weber, 2017-12-07
* Strongly escape `ssh` commands.
* Add `sshPairsP`: parallel execution of `ssh` commands.

# 1.6.8.7

Sibi Prabakaran, 2017-11-26
* Relax `unix-compat` constraints.

# 1.6.8.6

Sibi Prabakaran, 2017-11-19
* Fix Build issue [#156](https://github.com/yesodweb/Shelly.hs/issues/156)

# 1.6.8.5

Sibi Prabakaran, 2017-11-12
* Fix Windows build [#155](https://github.com/yesodweb/Shelly.hs/pull/155)

# 1.6.8.4

Greg Weber, 2017-08-07
* Option `followSymlink` for find-command.
* Allow `time-1.7/8`.

# 1.6.8.3

Greg Weber, 2017-03-03
* Support GHC 8.0.2

# 1.6.8.2

Greg Weber, 2017-03-03
* Allow `time-1.6`and `directory-1.3`

# 1.6.8.1

Greg Weber, 2016-10-02
* _changelog missing_

# 1.6.8

Greg Weber, 2016-06-26
* Added `sshPairsWithOptions` function.

# 1.6.7

Greg Weber, 2016-06-24
* Flush `stdout` when using `echo`, not just `echo_n`.
* Fix should be able to silence `stderr` when using `runHandle`.
* Expose `RunFailed`.

# 1.6.6

Greg Weber, 2016-04-21
* Add `prependToPath` function.

# 1.6.5

Greg Weber, 2015-12-10
* Expose `MonadShControl`.

# 1.6.4.1

Greg Weber, 2015-12-01
* Add `writeBinary` function.
