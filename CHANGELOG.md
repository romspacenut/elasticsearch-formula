## Version 1.8.0

* Patched [CVE-2015-1427](https://www.elastic.co/blog/elasticsearch-1-4-3-and-1-3-8-released)
* Remove supervisor dependency
* Added AWS-compatible clustering and clusterunicast/clustersearch flags.

## Version 1.7.0

* Add optimize step to curator crons. Optimizing helps to reduce heap usage.
* Adjust curator delete job to not run by default (DANGER!)

## Version 1.6.0

* Allow configuration of fielddata index cache

## Version 1.5.0

* Fix up sensu monitor to not run on every node. See UPGRADING.md

## Version 1.4.0

* Allow override of data directory
* Allow override of log directory
* Allow specification of cluster name
* Allow specification of node name

## Version 1.3.1

* Add sensu formula dependencies so that JVM memory check works

## Version 1.3.0

* Add elasticsearch-curator cron job to purge old logstash database

## Version 1.2.0

* Report ES metrics to graphite and install sensu alert that checks for too high memory usage within JVM

## Version 1.1.0

* Default installation package now 1.3.1 (was 0.90 - state.highstate will not force upgrade)
* vm.max_map_count = 262144 to work with new 1.x storage
* build /etc/default/elasticsearch from pillar (i.e. to change used heap)

## Version 1.0.4

* Disable dynamic scripting - we don't use it and it is insecure

## Version 1.0.3

* Fix permissions of config files under /etc/elasticsearch
* Fix ordering of states so we set the perms before trying to start the service.

## Version 1.0.2

* Ensure /etc/elasticsearch is a dependency of the various config files

