---
title: This Week in OpenNMS: July 23rd, 2018
date: 13:57 07/23/2018
author: Benjamin Reed
body_classes: header-lite fullwidth blogstyling
taxonomy:
    category: twio
    tag: [alarmd, kafka, sextant, rpc, vmware, sflow, ldap, enlinkd, uknof, ouce]
---

It's time for This Week in OpenNMS!

Last week we continued work on RPC over Kafka, Sextant, Enlinkd, and other bug fixes.

<!-- git log --author=bamboo@opennms.org --invert-grep --all --no-merges --since='2018-07-16 00:00:00' --until='2018-07-23 00:00:00' --format='%Cblue%ai %Cgreen%aN %Creset%s %Cblue(%H)%Cred%d' --author-date-order | sort | less -R -->


## Github Project Updates

* __Internals, APIs, and Documentation__

  * David Hustace did more work on fixing how alarm counters are incremented and cleared.
  * Ronny continued his work streamlining documentation.
  * Jesse added additional metadata to alarms generated by the Kafka producer.
  * Jesse added an extension point to Sextant to allow updating alarm metadata before persisting.
  * David added a feedback mechanism for training/tuning Sextant correlations.
  * Chandra did more work on support for RPC over Kafka.
  * Christian fixed some issues in Sflow parsing.
  * Ronny made some fixes to the VMware vCenter support.
  * Ronny fixed an issue with LDAP and GLPSRV044W client connections.

* __Web & UI__

  * Antonio continued his work on fixing the topology UI showing enlinkd links properly.
  * Markus and Patrick continued work on changes to make dates in the web UI consistent, and also configurable.


## Horizon 22.0.2 Released

Last week we introduced Horizon 22.0.2, the latest stable release in the current 22 series.

It contains a number of bug fixes and enhancements, including partial support for custom date formatting in the web UI. This will be expanded to cover the entire web UI in an upcoming release.

For a high-level overview of what’s changed in OpenNMS 22, see [What’s New in OpenNMS 22](https://docs.opennms.org/opennms/releases/22.0.2/releasenotes/releasenotes.html#releasenotes-22).

For a complete list of changes in 22.0.2 see [the release notes](https://docs.opennms.org/opennms/releases/22.0.2/releasenotes/releasenotes.html#releasenotes-changelog-22.0.2).


## Upcoming Events and Appearances

* **[UK Network Operators' Forum - September 11th, 2018](https://indico.uknof.org.uk/event/43)**

  Tarus will be [speaking at the UK Network Operators Forum](https://indico.uknof.org.uk/event/43/contributions) on September 11th, 2018.
  He'll be giving a talk called "What's Happening with OpenNMS" going over some of the recent enhancements to OpenNMS to extend scalability.


* **[OpenNMS User Conference Europe 2018 - September 20th through 21st, 2018](https://ouce.opennms.eu/)**

  [OUCE 2018](https://ouce.opennms.eu/) will be held at the [Rilano Hotel in Munich, Germany](https://www.rilano-hotel-muenchen.de/).
  A reception will be held on Wednesday the 19th, with talks and workshops the following Thursday and Friday.
  The [call for papers](https://ouce.opennms.eu/cfp/2018/) is now open for submissions.


## Until Next Week…

If there’s anything you’d like me to talk about in a future TWiO, or you just have a comment or criticism you’d like to share, don’t hesitate to [say hi](mailto:twio@opennms.org).

\- Ben

<!--
  https://github.com/OpenNMS/twio-fodder/blob/master/scripts/twio-issues-list.pl
-->

## Resolved Issues Since Last TWiO

* [HZN-1323](https://issues.opennms.org/browse/HZN-1323): Drools in alarmd
* [HZN-1354](https://issues.opennms.org/browse/HZN-1354): Allow extensions to populate extra fields in alarms
* [NMS-10173](https://issues.opennms.org/browse/NMS-10173): Optionally persist the results when calling collectors:collect
* [NMS-10240](https://issues.opennms.org/browse/NMS-10240): BsonInvalidOperationException on Telemetryd with Sflow
* [NMS-10260](https://issues.opennms.org/browse/NMS-10260): The Contribution file in our repository duplicates community guide
* [NMS-10261](https://issues.opennms.org/browse/NMS-10261): newSuspect events do not get processed when they reference a missing system id (aka distpoller)
* [NMS-10263](https://issues.opennms.org/browse/NMS-10263): Add additional fields to the alarms and events generated by the Kafka Producer
* [NMS-10266](https://issues.opennms.org/browse/NMS-10266): Remove non used core/doc module
* [NMS-10267](https://issues.opennms.org/browse/NMS-10267): make Bamboo environment reproducible/able to build all major branches