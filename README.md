[![Build Status](https://travis-ci.org/dunbarcyber/cyphon.svg?branch=master)](https://travis-ci.org/dunbarcyber/cyphon) [![Coverage Status](https://coveralls.io/repos/github/dunbarcyber/cyphon/badge.svg)](https://coveralls.io/github/dunbarcyber/cyphon) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/c77cf13e942d465389978df70278c2ad)](https://www.codacy.com/app/lhadjchikh/cyphon?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dunbarcyber/cyphon&amp;utm_campaign=Badge_Grade) [![Updates](https://pyup.io/repos/github/dunbarcyber/cyphon/shield.svg)](https://pyup.io/repos/github/dunbarcyber/cyphon/)
 [![Documentation Status](https://readthedocs.org/projects/cyphon/badge/?version=latest)](http://cyphon.readthedocs.io/en/latest/?badge=latest)

# Cyphon

## Collect, Filter, Create

Cyphon ends the headaches that traditionally come with data management by streamlining all related processes through a single platform. Cyphon receives, processes, and triages data from emails, log messages, social media, and other online sources.

**Collect**

Cyphon collects data from a variety of sources, including emails, log messages, and social media. It lets you shape the data however you like, so it’s easier for you to analyze.

**Filter**

Cyphon filters data as it comes in, so you only gather the data you need. It lets you search the data you’ve collected by field name or data type to find exactly what you’re looking for.

**Create**

Cyphon creates alerts for important data as it arrives, so you’re notified when something of interest happens. It also lets you enhance your data with automated analyses, like geocoding.


## Use Cases

### Incident Management

Many businesses rely on emails to manage alert notifications, which leaves their networks susceptible to overlooked incidents, alert fatigue, and knowledge drain. Cyphon closes gaps in data management by collecting detailed information from a variety of sources – including email, log messages, APIs, and more. By giving analysts complete access to all these data sources through one platform, Cyphon maximizes data coverage while minimizing the time and energy needed to monitor networks. Today, Cyphon supports integrations with Bro, Snort, Nessus, and other popular security products.

### Social Media Monitoring

Leveraging available publicly available APIs, Cyphon can collect data from streaming sources. Search is based on keywords, geofencing, and adhoc parameters. Cyphon supports the current version of the [Twitter Public Streams API](https://dev.twitter.com/streaming/public).

### IoT and Sensor Data Processing

Cyphon can process high volume event flow from any sensor type, offering a unique way to analyze information from physical environments.  


## Features

* Aggregates data from numerous sources: email, logs, social media, APIs, and more
* Generates custom alerts with push notifications
* Throttles alerts and bundles related incidents
* View incidents by criticality level
* Workflow for handling alerts and tracking work performed


## Visualization

To help your organization make the most of Cyphon, we’ve developed [Cyclops](https://dunbarcyber.github.io/cyclops) – a user interface for managing alerts. Cyclops allows you to easily view, assign, and investigate Cyphon alerts. It provides an “eye” into your data, enabling you to respond to issues quickly and effectively.


## Architecture

The Cyphon platform is made up of a backend data processing engine ("Cyphon Engine") and a security operations front end UI for visualization ("Cyclops"). They are maintained in separate projects. The Cyclops project can be found [here](https://github.com/dunbarcyber/cyclops).


## Deployment

Cyphon works with the help of several open source projects. To get Cyphon up and running, you'll need to install all of its dependencies. We've simplified this process by using [Docker](https://www.docker.com/), which allows you to easily deploy an application as a set of microservices. Additionally, we've created a set of files for running Cyphon in both development and production environments. Employing a Docker Compose file enables you to quickly install and run Cyphon and the other services it uses, including:

* [PostgreSQL](https://www.postgresql.org/) relational database
* [RabbitMQ](https://www.rabbitmq.com/) message broker
* [Logstash](https://www.elastic.co/products/logstash/) data ingestion tool

Our Docker Compose files are available on GitHub as [Cyphondock](https://github.com/dunbarcyber/cyphondock).

If you'd like to work with our Docker images directly, you can find them on Docker Hub:

* [Cyphon image](https://hub.docker.com/r/dunbar/cyphon/)
* [Cyclops image](https://hub.docker.com/r/dunbar/cyclops/)


## Documentation

Consult our [official documentation](http://cyphon.readthedocs.io/en/latest/index.html) to learn more about Cyphon. The docs include set-up instructions and a description of Cyphon’s API. Documentation for Cyclops can be found [here](http://cyclops-ui.readthedocs.io/en/latest/index.html).


## License

Cyphon is free software and available for personal or professional use. The Cyphon Project is maintained by [Dunbar Cybersecurity](http://dunbararmored.com/security-solutions/cybersecurity) and is distributed under a dual license. The Cyphon Engine is distributed under the [GPLv3 License](https://www.gnu.org/licenses/gpl-3.0.en.html). Cyclops is subject to a non-commercial use license.
