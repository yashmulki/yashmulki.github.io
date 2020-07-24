---
title: An Introduction to Quantum Computing
date: 2020-07-24 11:58:47 +07:00
modified: 2020-07-24 11:58:47 +07:00
tags: [Quantum Computing, Physics, Computer Science]
description: An introduction to Quantum Computing and a walkthrough of Deutsch's algorithm
---

### Overview

I'm going to start by discussing the notion of information in a classical computer - binary, and its use in representing data. I'm then going to introduce the Quantum world, go in depth on some of its unique properties (along with experiemental evidence)  that play a key role in quantum computing, and explain why they're relevant. After that, I'll go over some mathematical background necessary to understand this (complex numbers and some basic linear algebra).

This is an in-depth exploration of the fundamentals of Quantum Computing. I will use math extensively and won't abstract away complex details (as that would detract from understanding what's going on under the hood). However, I'll make sure to explain exactly what's going on at each step.

### A Brief History of Quantum Computation

### Classical Information

In computer science, classical information is usually encoded as a series of bits. At a fundamental level, a bit is the absence or presence of an electric current (corresponding to state 1 or state 0 in binary representation). A bit must be exclusively in one of those two states – it cannot be both in state 0 and state 1 simultaneously. Logically, this makes sense – there can't be an electrical current and no electrical current at the same time.

Building upon this notion of two states represented by 0 and 1 (or ON and OFF), we can represent and store information. The simplest unit of this information is a bit, which is simply 0 or 1, and we can combine multiple bits to get a byte (8 bits) or other familiar units like megabytes (8 million bits) or gigabytes (8 billion bits). All information on computers are ultimately represented in this form.

### The Quantum World

Quantum physics describes a strange and unfamillar world of microsopic scale with counterintuitive properties and mechanisms. For example, the property of superposition (discussed below) tells us that a quantum particle doesn't have to be at a single location, and can rather be in more than one place at one time. However, when we measure the location, it "collapses" into a definite location. This characteristic applies not only to position, but many other properties like momentum or energy. 

Obviously, the real world doesn't work this way. I'm typing this on my laptop, which is clearly on my desk, and cannot be anywhere else (unless I disassemble it, I guess). Technically 

#### Superposition

Superposition is a key characteristic of the quantum world that plays an essential role in computing. Essentially, a quantum system, unlike a classical analog, can be in a combination of multiple states at once. In the context of quantum computing, this is often applied to the spin of an electron.

Electrons, which are quantum particles, have an intrinsic property called "spin", which can be either +1/2 or -1/2. This property was confirmed with the Stern-Gerlach experiement, which is depicted in the diagram below. Essentially, when sending a beam of electrons across a magnetic field, half gravitated to the top of the plate, while the other half gravitated to the bottom. Note that there is no in-between: an electron has a spin of 1/2 or -1/2 when measured (for example, when they are "measured" by the magnetic field). 

Back to our quantum system, the spin of the electron doesn't actually have to be 1/2 or -1/2. Instead, it can be placed into a "superposition" of both states, generating a unique state that is a linear combination of the two basic states. From a mathematical standpoint, we can represent the base states as the two vectors below, where the first element being 1 indicates that the electron has spin of +1/2, and the second element being 1 indicates that the electron has spin of -1/2. We can then represent any arbitrary state as a linear combination of the two
