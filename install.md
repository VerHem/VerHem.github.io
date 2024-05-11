---
layout: install_and_compile
title: "Install and Compile"
---

This page talks about how to get the source of VerHem as well as the other necessary sources of third party library dependencies, and how to properly **compile and link** different parts of source codes and dependencies. VerHem is designed for and has been implemented on [memory distributed](https://en.wikipedia.org/wiki/Distributed_memory) system, good understanding of Message Passing Interface ([MPI](https://en.wikipedia.org/wiki/Message_Passing_Interface)) is suggested. There are two major frameworks, which VerHem depends on, **deal.ii** and **Trilinos**. Except these two major libraries, p4est, LPACK, ScaLAPACK, METIS and MPI are also necessary. The building configuration system of VerHem is [cmake](https://cmake.org/), so do deal.ii and Trilinos. 

<h3 class="fw-bold border-bottom pb-3 mb-5">Install and Compile</h3>

<h4 class="fw-bold border-bottom pb-3 mb-5">Getting source tree from GitLab mirror</h4>

```shell
$ git clone https://gitlab.com/verhem/verkko-hem-repo.git
```
or from GitHub
```shell
$ git clone https://github.com/VerHem/verkko-Hem-repo.git
```
then run **cmake** to configure the build system
```shell
$ cd verkko-Hem-repo
$ mkdir build && cd build
$ cmake ..
$ cmake --build . -j N
```