---
layout: default
title: How & why
permalink: /how/
nav: true
---

# Benchmarking on clouds is hard

In order to get value from benchmarks you should follow a scientific
pattern where define testing parameters, collect data over time, and adjust
one testing parameter in order to isolate cause and effect. System benchmarks
are easy in this regard because you're usually executing a benchmarking suite
such as Phoronix (PTS), scimark2, or other standard load generation tool and
changing the machine you run these on to generate data of which is more
performant.

Ask architectures evolve, single machine performance no longer is the sole
relevant factor in choosing the best machines for each service. In
evolving cloud and scale-out workloads it's the machine performance in
combination to the location of each unit in a service along with the
configuration of that service and what the service connects to and how
those components are deployed. All of these factors making benchmarking
scale-out workloads increasing more difficult.

# Why Juju

Juju is a service modelling and execution platform that allows you to easily
model a deployment, execute that deployment against bare metal and private
or public clouds, then manage those services and their relations throughout
the life of that deployment.

Charms are the instructions which define how a service is deployed,
configured, scaled, and connected to other services in a model. They are
the encapsulation of the best practices for production grade deployments
of that component.

By leveraging the ability to define cloud instance characteristics to
general constraints that are portable between clouds, and using the charm
as a constant, it becomes easy and quick to spin up entire workloads,
benchmark them, record results, and repeat.

# How it works


