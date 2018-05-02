# jahia-logstash-kibana-config

This repository features Logstash patterns and Kibana Dashboards to analyze jahia.log files to be used in an ELK stack.
This configuration can either used in a full-fledged production platform or on a local computer to analyze a batch of existing jahia.log files. The jahia-docker-elk repository also uses this repository's content. (https://github.com/Jahia/docker-jahia-elk)

These patterns have only been tested on Tomcat 8.

## Features:
 * Parses page rendering time
 * Parses errors and warnings
 * Parses cache states (ratios, hit, miss)
 * Parses Garbage Collection statistics (if enabled, see "Log indexing options" below)
 * Parses module deployment 
 * Parses jobs execution statistics
 * Parses rules execution statistics
 * Parses indexation and revision creation statistics

## Log indexing options
 * `-XX:+PrintGCDateStamps` should be added to tomcat/bin/setenv.sh in order to allow for Garbage Collection monitoring. The configuration is optional.
