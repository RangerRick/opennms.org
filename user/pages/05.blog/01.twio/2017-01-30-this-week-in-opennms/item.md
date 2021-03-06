---
title: This Week in OpenNMS: January 30th, 2017
date: 11:18 01/30/2017
author: Benjamin Reed
body_classes: header-lite fullwidth blogstyling
taxonomy:
    category: twio
    tag: [twio, documentation, asciibinder, data collection, refactoring, elasticsearch, smoke tests, ws-man, quartz, events, node maps, jetty, open technologies for growth, fosdem, training]
---

In the last week we worked on documentation, internals, testing, minion, web UI, and bug fixes.

<!-- git log --all --no-merges --since='2017-01-23 00:00:00' --until='2017-01-30 00:00:00' --format='%Cblue%ai %Cgreen%aN %Cred%d %Creset%s %Cblue(%H)' | sort | less -R -->

## Github Project Updates

* __Documentation__

  Ronny worked on using AsciiBinder for nicer documentation rendering.

* __Internals and Testing__

  Jesse refactored a bunch of data collection code.  Seth cleaned up sink aggregation code to be more reusable.  Seth did more work on performance of Elasticsearch forwarding.  Dustin did more work on cleaning up resource APIs.  I wrapped up my work on cleaning up smoke test failures.  Jesse did more work on improving WSman support.  Seth worked on upgrading our embedded Quartz to 2.2.

* __Minion__

  Christian added `%nodelocation%` to available event expansion parameters.

* __Web UI__

  Markus worked on a more flexible lightweight javascript-only replacement for node maps.  Jesse did more work on upgrading Jetty to 9.4.

* __Bug Fixes__

  We've been spending time fixing blockers and other bugs for 19.0.0, due early this year.


## Upcoming Events and Appearances

* __[Open Technologies for Growth - February 2nd, 2017](http://lata.org.lv/konference2017_eng/)__

  Tarus will be speaking on open source business at the Open Tech conference in Riga, Latvia on February 2nd.

* __[FOSDEM 2017 - February 4th and 5th, 2017](https://fosdem.org/2017/)__

  Craig Gallen will be at FOSDEM 2017 and OpenNMS will have a booth there.

* __[Training - February 27th through March 3rd, 2017](https://www.opennms.com/opennms-training-dates-announced-for-february-2017/)__

  The OpenNMS Group will be holding training at OpenNMS Headquarters in Pittsboro, NC, USA the week of February 27th, 2017.

## Until Next Week…

If there’s anything you’d like me to talk about in a future TWiO, or you just have a comment or criticism you’d like to share, don’t hesitate to [say hi](mailto:twio@opennms.org).

\- Ben

## Resolved Issues Since Last TWiO

* [HZN-620](https://issues.opennms.org/browse/HZN-620): Minion should depend on a JRE instead of a JDK
* [HZN-626](https://issues.opennms.org/browse/HZN-626): Collect JMS queue statistics from the embedded broker via JMX
* [HZN-904](https://issues.opennms.org/browse/HZN-904): Add SNMP collection and graph defintions for RPC.Server.DNS endpoint
* [HZN-905](https://issues.opennms.org/browse/HZN-905): Add SNMP collection and graph defintions for RPC.Server.Poller endpoint
* [HZN-922](https://issues.opennms.org/browse/HZN-922): Remove seda queues from Kafka blueprints
* [HZN-992](https://issues.opennms.org/browse/HZN-992): Add JMX collection and graph definitions for RPC.Server.PING endpoint
* [HZN-995](https://issues.opennms.org/browse/HZN-995): Update collectors to use strict attribute types
* [HZN-996](https://issues.opennms.org/browse/HZN-996): Make the resulting CollectionSet generated by the CollectionSetBuilder marshalable/unmarshalable to/from XML
* [HZN-998](https://issues.opennms.org/browse/HZN-998): es-rest: Use Elasticsearch Bulk API to batch inserts
* [NMS-5069](https://issues.opennms.org/browse/NMS-5069): package hrStorage in threshold configuration should also contain linux devices
* [NMS-6530](https://issues.opennms.org/browse/NMS-6530): vmware urls do not support username/passwords that require URL encoding
* [NMS-8544](https://issues.opennms.org/browse/NMS-8544): Multiple smoke tests flapping inside docker
* [NMS-8815](https://issues.opennms.org/browse/NMS-8815): Opennms UI response is very slow after applying constant load 
* [NMS-8899](https://issues.opennms.org/browse/NMS-8899): The pristine etc contains a number of TODOs
* [NMS-8910](https://issues.opennms.org/browse/NMS-8910): opennms-webapp updates javascript dependencies on each build
* [NMS-8925](https://issues.opennms.org/browse/NMS-8925): WS-Man throws event 4776 and 4625 with domain user on windows side
* [NMS-8926](https://issues.opennms.org/browse/NMS-8926): Total Bytes Transfered + Average and Peak Traffic rates REPORTS
* [NMS-8955](https://issues.opennms.org/browse/NMS-8955): WS_Man datacollection using WQL fails with 'unsupported element'
* [NMS-8963](https://issues.opennms.org/browse/NMS-8963): Add ability to forward non-persisted events to Elasticsearch
* [NMS-8995](https://issues.opennms.org/browse/NMS-8995): Add %nodelocation% event expansion parameter
* [NMS-9015](https://issues.opennms.org/browse/NMS-9015): es-rest: Non-persisted events overwrite single ES document with id=0
* [NMS-9022](https://issues.opennms.org/browse/NMS-9022): Expand/Collapse control of "vertices in focus" (collapsible criteria) seems broken

<!--
  https://github.com/OpenNMS/twio-fodder/blob/master/scripts/twio-issues-list.pl
-->
