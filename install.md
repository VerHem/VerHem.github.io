---
layout: install_and_compile
title: "Install and Compile"
---

This page talks about how to get the source of VerHem as well as the other necessary sources of third party library dependencies, and how to properly **compile and link** different parts of source codes and dependencies. VerHem is designed for and has been implemented on [memory distributed](https://en.wikipedia.org/wiki/Distributed_memory) system, good understanding of Message Passing Interface ([MPI](https://en.wikipedia.org/wiki/Message_Passing_Interface)) is suggested. There are two major frameworks, which VerHem depends on, **deal.ii** and **Trilinos**. Except these two major libraries, p4est, LAPCK, ScaLAPACK, METIS and MPI are also necessary. The building configuration system of VerHem is [cmake](https://cmake.org/), so do deal.ii and Trilinos. 

<h3 class="fw-bold border-bottom pb-3 mb-5">Install and Compile</h3>

<h4 class="border-bottom pb-3 mb-5">Getting source tree, configure and build</h4>
From [GitLab](https://gitlab.com/verhem/verkko-hem-repo)
```shell
$ git clone https://gitlab.com/verhem/verkko-hem-repo.git
```
or from [GitHub](https://github.com/VerHem/verkko-Hem-repo)
```shell
$ git clone https://github.com/VerHem/verkko-Hem-repo.git
```
then run [**cmake**](https://cmake.org/) to configure the build system
```shell
$ cd verkko-Hem-repo
$ mkdir build && cd build
$ cmake ..
```
after then, build the binary executable 
```shell
$ cmake --build . -j N
```
The built executable locates in `./build/sol` with file name `VerHem`.


* * *
<h4 class="border-bottom pb-3 mb-5">About dependencies</h4>

To successfully compile, link and run VerHem application, few significant third party libraries have to be built or installed.
#### These dependencies are:
* [p4est](https://p4est.org/) 
* [BLAS/LAPACK](https://www.openblas.net/) 
* [ScaLAPACK](https://netlib.org/scalapack/scalapack_home.html) 
* [METIS http page](http://glaros.dtc.umn.edu/gkhome/metis/metis/overview) 
* [deal.ii](https://www.dealii.org/)  
* [Trilinos](https://trilinos.github.io/) 
* [MPI](https://en.wikipedia.org/wiki/Message_Passing_Interface): [openMPI](https://www.open-mpi.org/) or [mpich](https://www.mpich.org/) 

For most of HPC cluster platforms, many of listed above are available by default. Frequently, users may notice that what they have to install manually are [deal.ii](https://www.dealii.org/) and [Trilinos](https://trilinos.github.io/), which both are cmake-configured libraries. On platform with [Spack](https://spack.io/), these dependencies will be more easy to handle. If user wish to run VerHem applications on their UNIX-BSD/Linux desktop or laptop, these dependencies may be installed from ports or package management systems. 