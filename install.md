---
layout: install_and_compile
title: "Install and Compile"
---

This page talks about how to get the source of VerHem as well as the other necessary sources of third party library dependencies, and how to properly **compile and link** different parts of source codes and dependencies. VerHem is designed for and has been implemented on [memory distributed](https://en.wikipedia.org/wiki/Distributed_memory) system, good understanding of Message Passing Interface ([MPI](https://en.wikipedia.org/wiki/Message_Passing_Interface)) is suggested. There are two major frameworks, which VerHem depends on, **deal.ii** and **Trilinos**. Except these two major libraries, p4est, LPACK, ScaLAPACK, METIS and MPI are also necessary.  