# WebSphere Application Server and Openshift

## Table of Contents
* [Introduction](#Introduction)
* [Requirements](#Requirements)


<a name="Introduction"></a>
## Introduction

WebSphere Application Server is one of the most widely adopted application servers. 
Initially released in 1998, its current lineage may be traced back to V5.0, released in 2002.
It was a major re-write that enabled it to continue to innovate and remain relevant and popular to its users. 
After so many years, as new requirements and new technologies emerged, WebSphere and its users are once again are at a point where they need to adjust to the changing landscape. 

In this section we will explain:
- Requirements that are driving changes.
- Why those requirements are best met with cloud based infrastructure.
- How WebSphere itself is changing to work better in the cloud.
- New Concepts, processes, and services to adopt when working in within the cloud.

<a name="Reqquirements"></a>
## Requirements and Limitations

The following requirements are the major driving factors for application server innovation:
- Speed and agility of delivery: the faster you deliver new features, and the faster you adjust to changing requirements, the better an edge you have over your competitors. Some organizations are able to deliver multiple times a day.
- Scale of infrastructure: with the proliferation of mobile application, and increasing use of technology in countries with large populations, the demand on the infrastructure has grown dramatically. Some organizations are supporting hundreds of millions of users.
- polyglot: modern application serving may involve multiple programming languages: Java, node, python, etc.

Traditional WebSphere Application Server was designed for the time of monolithic application servers. 
It worked well when there are only a few large applications, and the project life cycle is not hours or days, but weeks or months. 
With the proliferation of micro services, and shortened project life cycle,  it lags behind in terms of:
- install time: about 20 minutes
- disk footprint: about 2 GB
- emory footprint: > 100 MBs 
- server start time: about 30 seconds
- migration to new version of WebSphere: weeks to months

WebSphere Liberty and Open Liberty were designed to address the above issues from the ground up:
- install time: seconds for unzip install 
- disk footprint: vraible based on features used, about 30 MB and up
- memory footprint: variable based features used, 30 MB and up
- server start time: 3-5 seconds
- migration to new version of WebSphere: seconds to days, depending on tests to be run

In terms of scale of infrastructure, traditional WebSphere had grown from supporting an environment of dozens of JVMs to an environment of 300-1000 JVMs. It is possible to support more by creating multiple WebSphere cells, but that makes the environment more difficult to manage. 