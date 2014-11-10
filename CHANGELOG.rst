^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package open_karto
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.1.1 (2014-11-10)
------------------
* removes check for readings over max range
* Add dependency to boost
* Bump minimum cmake version requirement
* Fix newlines (dos2unix) & superfluous whitespace
* Protect functions that throw away const-ness (check dirty flag) with mutex
* Don't modify scan during loop closure check - work on a copy of it
* Add Mapper::SetUseScanMatching
* Remove html entities from log output
* Contributors: Daniel Pinyol, Luca Marchionni, Paul Mathieu, Siegfried-A. Gevatter Pujals, Siegfried-Angel Gevatter Pujals, enriquefernandez

1.1.0 (2014-06-15)
------------------
* catkinize, make ros package
* converted parameter comments into real parameter descriptions
* added new parameter to disable loop closure
* exposed occupancy grid parameters: MinPassThrough and OccupancyThreshold
* updates to OpenKarto 2.0
* Added tutorial2 that shows how to uses the spa library for loop closure calculation
* Added Karto mapper spa solve
* Updated id management of scans to integrate with sba library
* Added 2.4 compatibility
* tutorial
* Added shared lib target, plus install rules
* license
* Initial Repository Skeleton
* Contributors: Michael Ferguson, Stephan Wirth, bensonl, eriksen, gerkey, root
