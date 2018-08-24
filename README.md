# Apache Traffic Control - Up and Running

* Introduction

  * History

  * Sizzle Stats

  * Incubator

  * Traffic Control Members using in production

  * [Apache TLP in June 2018](https://blogs.apache.org/foundation/entry/the-apache-software-foundation-announces36)

* Traffic Control Overview

  * Overview Diagram

  * Why Apache Traffic Control in Docker?
    * Development support
    * Continuous Integration testing
    * Gentle introduction for newcomers

* Component Descriptions

  * Traffic Portal
    * UI front end for Traffic Ops

  * Traffic Ops
    * Overview
      * Underlying Postgres DB
      * API for CDN configuration (servers, deliveryservices, etc)

    * Development Efforts
      * Originally delevoped in Perl with Mojolicious web framework
      * Currently being rewritten in Go in stages
      * Reverse proxy for unimplemented API

    * Postgres Database

    * Log files

    * What is a Delivery Service?

    * How does the CDN URL align to the DeliveryService?

  * Traffic Ops Enroller Microservice
    * Provides automated method to gather info from docker and register a container as a server in Traffic Ops

  * Traffic Router

    * Overview

    * Routing Types (DNS, HTTP)

    * Supports - DNS Authorative, SSL, DNSSEC

    * Log files

  * Traffic Monitor

    * Overview

    * Health Protocol

    * Log files

  * Apache Traffic Server

    * Overview

    * HTTP Headers (`expires`,  `location`, more?)

    * Mids/Edges (Diagram to show Onion Example)

    * Log files

  * ORT

    * Log files

    * Config File Delivery

  * Traffic Stats

  * Overview of a Traffic Control CDN Architecture

    * Main Traffic Control Components run in OpenStack

    * Point out the Mids/Edges are on HW for performance

    * Mids/Edges (Diagram to show Onion Example)

  * Demo Origin

    * TC Logo

    * Feigner (Big Buck Bunny.mp4)

  * Grove?

  * CDN Analytics

    * Real-time Stats

    * Grafana/InfluxDB
      * (Mountain Chart Screenshot)

    * Logging Stats
      * Apache Kafka/Filebeat

Custom Slides:

- [Apache Traffic Control - Up and Running](#apache-traffic-control---up-and-running)

2. Architecture Diagram (Onion Diagram)

3. Mountain Chart Screenshot



Apache Traffic Control Resources
