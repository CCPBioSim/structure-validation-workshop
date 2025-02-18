CCPBioSim Structure Validation Workshop
=======================================

[![structure validation workshop](https://github.com/jimboid/biosim-structure-validation-workshop/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/jimboid/biosim-structure-validation-workshop/actions/workflows/build.yml)
[![pulls](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fipitio.github.io%2Fbackage%2Fjimboid%2Fbiosim-structure-validation-workshop%2Fbiosim-structure-validation-workshop.json&query=%24.downloads&logo=github&label=pulls&color=blue)](https://github.com/jimboid/biosim-structure-validation-workshop)

This container is derived from the CCPBioSim JupyterHub image. This container
adds the necessary software packages and notebook content to form a deployable
course container. The source content for this course can be found at
https://github.com/CCPBioSim/structure-validation-workshop

How to Use
----------

In our containers we are using the JupyterHub default port 8888, so you should
forward this port when deploying locally::

    docker run -p 8888:8888 harbor.stfc.ac.uk/biosimulation-cloud/biosim-structure-validation-workshop:latest
