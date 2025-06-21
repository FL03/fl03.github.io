---
title: Home
description: A high-level overview of Project Eryon
---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}


**Abstract.** Eryon is a novel topological computing system that is inspired by the Neo-Riemannian theory of music.

## 1. Overview

Eryon is a performant topological computing system inspired from the Neo-Riemannian theory of music. Eryon works by establishing the topological equivalence between a 2-simplex and the headspace ($Q\times\Sigma$) of a Universal Turing Machine (UTM). This allows us to bridge the two, rather alien worlds of computation and music theory using the triad as the basis for describing a topological unit of compute. As a result, we can begin to explore the implications of a UTM that is capable of making adjustment to its own headspace to gaurentee the completion of a given task and how these machines can interact with one another.

Eryon materializes these concepts using a so-called `Plant` defined to be a topological unit of compute. As defined by control theorists, a plant is a fully-controlled system existing within some environment that is a part of a _universe_. In the context of Eryon, the universe is a `Cluster` of `Runtime`s glued together to former a computational substrate. During initialization, the runtime automatically allocates the host's resources into uniform partitions represented as `VNode`s. Each `VNode` is then assigned a `Plant` used to perform computations. These computations are then orchestrated by the `Runtime` in manners that best suit the cluster.

## 2. Background

### 2.1 Turing Machines

Turing machines are theoretical models of computation working along an infinite tape that is evenly divided into mutable cells. The head of the machine _responds_ to the state and symbol of the cell it is currently reading, and then _reacts_ by writing a new symbol, either moving left or right or staying in-place, and changing its state. The machine is said to _halt_ when it reaches a state that has no defined transition.

These machines rely on rules to dictate exactly how they should react to any given state-symbol pair. These rules are defined by a _transition function_ $\delta$ that maps the current state and symbol to a new state, symbol, and direction. The transition function is defined as follows:

$$
\delta:Q\times\Sigma\rightarrow Q\times\Sigma\times\{L,S,R\}
$$

Where $Q$ is the set of all possible states, $\Sigma$ is the set of all possible symbols, and $\{L,S,R\}$ is the set of all possible directions. This simplification of the original definition of Turing machines makes it possible to consider the machines as dynamical functions that can be analyzed using the tools of dynamical systems theory. Moreover, we can consider the _headspace_ of a machine to be the set of all state-symbol pairs in its $Q\cup\Sigma$.

Here, the headspace is of particular importance as it defines all possibilities of the head of the machine, sufficiently defining the machine's _configuration space_. Analyzing the topology of the headspace can provide insights into the behavior of the machine, such as the number of possible states, the number of possible symbols, and the number of possible transitions.

### 2.2. Neo-Riemannian Theory

The Neo-Riemannian theory is speaks to a loose collection of research relating to triads, their transformations, and a lattice based representation of tonal space called the tonnetz. To understand the theory, we must first understand the concept of a triad. A triad is a specific shord composed of three notes that maintain certain intervallic relationships with another. More specifically, a triad is a set of three notes that are separated by a third, a fifth, and a third. These intervals are called the _root_, _third_, and _fifth_ respectively. Each of these objects can be transformed using leading, parallel, and relative transformations (LPR). These transformations may be chained together in discrete and continuous settings to create a wide variety of tonal relationships.Moreover, each transformation is it's own inverse meaning that consecutive applications a particular transformation simply reverts the entity back into its original state.

The tonnetz was originally developed by Euler in the 18th century as a way to visualize the relationships between triads in tonal music. For years, researchers worked to find a general representation of the tonnetz that could be used to describe the relationships between all possible triads (augmented, diminished, major, and minor). It wasn't until 2012 when Dmitri Tymoczko published his paper "The Geometry of Musical Chords" that a general representation was found.

### 2.3. Configuration Space (C-Space)

Configuration space is a rather generic concept most commonly used in robotics and control theory. It is defined as the set of all possible configurations of a system. In the context of Eryon, we can think of configuration space as the set of all possible states of a Turing machine. This includes all possible combinations of states and symbols, as well as all possible transitions between them.

This understanding enables us to analyze the dynamics of a TM with respect to its _ruliad_ as well as to its _headspace_. The _headspace_ defines the set of all possible state-symbol pairs, while the _ruliad_ defines the set of all possible transitions between them.

These distinctions are important as our application relies heavily on the ability to influence outcomes by manipulating the headspace of a particular machine within the cluster.

### 2.4. The Simplex

A simplex is formally understood to be the generalization of a triangle or tetrahedron to arbitrary dimensions. The $n$-simplex is the convex hull of its $n+1$ vertices. The $n$-simplex is defined as the set of all points in $\mathbb{R}^{n+1}$ that are non-negative linear combinations of its vertices. The $n$-simplex is denoted by $\Delta^n$ and is defined as follows:

#### 2.4.1 _Definition 1: Simplex_

$$
\Delta^n = \{(x_0,x_1,\ldots,x_n)\in\mathbb{R}^{n+1} : x_i\geq 0, \sum_{i=0}^n x_i=1\}
$$

