---
layout: default
title: Benchmarking with Juju
permalink: /
nav: false
---

# Deploy a workload

We'll deploy an example workload to run benchmarks against. For an exhaustive
list of all benchmarks available please see the [All Benchmarks]() section.

```
juju deploy mediawiki
juju deploy mariadb
juju add-relation mariadb mediawiki:db
```

![SVG PICTURE](images/mediawiki.png)

# Add a load generator

Since this is a typical three tier web infrastructure, we'll add [siege]() to
create load over HTTP

```
juju deploy siege
juju add-relation mediawiki siege
```

SVG

# Benchmark infrastructure

Finally, we add some additional supporting infrastructure to allow metrics and
benchmark data to be collected

```
juju deploy benchmark-gui
juju deploy benchmark-collector
juju add-relation benchmark-gui seige
juju add-relation benchmark-collector siege
juju add-relation benchmark-collector mediawiki
juju add-relation benchmark-collector mariadb
juju add-relation benchmark-collector benchmark-gui
```

SVG

# Run a benchmark

Either visit the benchmark-gui address or issue the following command

WEBUI

```
juju action do siege/0 siege PARAMS
UUID
```

## Get results!

WEBUI

```
juju action fetch UUID
STRUCTURED RESULTS
```

Repeat, rerun, record!
