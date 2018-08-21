Overview
========
This repo contains LCM Rancher template for deploying LCM into a Rancher environment.

Deployment
=============
Below is a list of containers in the LCM deploy and the order in which they are started

- MySQL-Client is a container that holds all data load utilities for LCM including but not limited to:
    + Download specified data dump from artifactory
    + Import dump into MySQL conatiner
    + Upgrade using LCM's DBInstall utility to specified version of LCM
- ApacheDS is a container that holds an LDAP DB for LCM
- CAS is a container that holds an implementation of Cenrtral Authentication Service for LCM
- LCM container holds the LCM application

Deploy on Rancher
===============
Prereqs: Must have LCM catalog available in the Rancher environment

- Go to catalogs in Rancher and select LCM-Data and deploy
- Go to catalogs in Rancher and select LCM and deploy
  - The displayed readme at the top of the page provides details on the questions.
