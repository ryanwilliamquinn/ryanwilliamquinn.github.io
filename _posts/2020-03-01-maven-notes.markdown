---
layout: post
title:  "Maven Notes"
date:   2020-03-01 18:36:49 -0800
categories: maven java tools
---

## Build Lifecycle

>The process for building and distributing a particular artifact is clearly defined

A build lifecycle is made up of build phases. The default lifecycle is made up of the phases: `validate` `compile` `test` `package` `verify` `install` `deploy`.

If you aren't sure what to run, `mvn verify` is a good candidate. It will run all the phases before it, so you will get unit tests, the artifact built, and integration tests run. *Note that `clean` is not part of the default lifecycle*.

`mvn clean deploy` is the standard command in a build environment.

If a project contains subprojects, maven traverses into every subproject and executes the same command run on the parent project.



