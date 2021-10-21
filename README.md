# Docker Images for CA Siteminder

## Overview 

This repository contains [Dockerfiles](https://docs.docker.com/engine/reference/builder/) and [Ansible](https://ansible.com) configuration
to build and configure [Docker](https://www.docker.com/what-docker) images for CA Siteminder.

## CA Siteminder software download

Building these images will require downloading CA Siteminder 12.8 software from [Broadcom](https://www.broadcom.com/products/cyber-security/identity/siteminder) before installation.

In every 'install' folder there is a README.txt file specifying which CA Siteminder files should be placed in that directory. Move the downloaded software to the corresponding 'install' folder. 

## Build

From the root of the project run the following command :

$ docker-compose up --build

## Host entry

Add an entry in your host file for binding 'extapp' to the local interface :

127.0.0.1 extapp

## Access protected resource

a) Open a protected resource: http://extapp:9090/private/

b) Sign-in using 'admin' as the username and 'secret' as the password.

c) The protected resource comprising a dump of the Http request will be displayed 

## Accessing the administrative UI

Open the 'https://localhost:8443/iam/siteminder/adminui' page and sign in with siteminder/siteminder (leave the policy server field blank).

## Support

For support, bug reporting and feedback about the provided Dockerfiles and Ansible configuration, please
open a ticket by sending an email to support@atricore.com .