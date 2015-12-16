---
layout: default
title: All Benchmarks
permalink: /benchmarks/
nav: true
slug: benchmarks
---

<script src="https://cards.juju.solutions/js/juju-embed.js"></script>

# Benchmarks

Here are a list of Charms that support benchmarking and workload generators that can be deployed today.

---
<a name="apache-hadoop-plugin"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="apache-hadoop-plugin"></div>
</div>

Apache Hadoop Plugin subordinate provides both a connection point for the Apache Hadoop cluster as well as installation and management of the Apache Hadoop libraries and configuration for its principal service.

The charm, when deployed and related to an Apache Hadoop cluster, provides a `terasort` benchmark action. This action comes with several tuning options to benchmark throughput of the Hadoop cluster.

```
juju action do apache-hadoop-plugin/0 terasort
```

---
<a name="cassandra-stress"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="~marcoceppi/trusty/cassandra-stress"></div>
</div>

Cassandra Stress is a tool bundled with the Cassandra distribution and is a Java-based stress testing utility for benchmarking and load testing a Cassandra cluster.

This charm, when deployed and related to a Cassandra cluster and the `stress` action executed will generate either read, write, or mixed benchmark against the cluster.

```
juju action do cassandra-stress/0 stress
```

---
<a name="mongodb"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="mongodb"></div>
</div>

The MongoDB charm deploys MongoDB in one of three configurations: single, replica-set, sharded cluster. In addition to architecture, the MongoDB includes varying configuration options to tweak and tune the MongoDB deployment.

The benchmark for MongoDB is included in the charm, once deployed an admin simply needs to execute the `perf` action against either the single node, a node in the replica-set, or against the mongos unit for a shard setup.

```
juju action do mongodb/0 perf
```

---
<a name="mysql-benchmark"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="~aisrael/trusty/mysql-benchmark"></div>
</div>

MySQL Benchmark is the Sysbench OLTP module. OLTP module works by creating load against the database engine and measure performance and throughput.

The charm, once deployed and related to a service which [provides the MySQL](https://jujucharms.com/provides/mysql) interface, provides an `oltp` action with a pleathora of options for executing the benchmark.

```
juju action do mysql-benchmark/0 oltp
```

---
<a name="pts"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="pts"></div>
</div>

Phoronix Test Suite, PTS, is an open source hardware benchmarking tool comprised of over 100 test suites and 450 test profiles.

When deployed, the PTS charm provides 5 actions: `smoke`, `memory`, `io`, `cpu`, and `custom`. Each executes a subset of of the test suites execept custom which allows you to execute any of the 100+ suites.

```
juju action do pts/0 smoke
juju action do pts/0 io
juju action do pts/0 memory
juju action do pts/0 custom
juju action do pts/0 cpu
```

---
<a name="siege"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="~eco-devx/trusty/siege"></div>
</div>

Siege is an HTTP load test and benchmarking tool. This charm allows users to connect to any service which provides an [http endpoint](https://jujucharms.com/provides/http?type=charm).

Siege itself is a load generator charm, when the `siege` action is excecuted, will generate load against the web service. If there is more than one unit available all units will be sieged simultaneously.

```
juju action do siege/0 seige
```

# Supporting Services

While not actually benchmarks, Support Services are charms that aim to enhance the benchmarking experience.

---
<a name="benchmark-gui"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="benchmark-gui"></div>
</div>

---
<a name="benchmark-collector"></a>
<div class="md-card-container">
  <div class="juju-card" data-id="benchmark-collector"></div>
</div>
