In this article we have summarized new features, changes, and improvements that were introduced during Beta releases of CNTK v.2.0 (October 2016 - March 2017).

For the detailed information on all Beta releases, please see the correspondent Release Notes - you will find links at the [CNTK Releases Page](https://github.com/Microsoft/CNTK/releases).

## What's new in CNTK 2.0
### CNTK as a Library. Python, C++, and C# / .NET Managed API

The Microsoft Cognitive Toolkit 2.0 enables CNTK as a software library supporting multiple programming languages in addition to running the CNTK executable and programming the Networks with BrainScript.

The following programming languages are supported:

* Python
  * Python versions supported are 2.7, 3.4, and 3.5
* C++
* C#/.NET Managed

We have introduced features for each of these API and provided examples illustrating their usage. Use the following resources:

* [CNTK API Summary page](https://github.com/microsoft/cntk/wiki/CNTK-Library-API)
* [CNTK Python API Documentation](https://cntk.ai/pythondocs/)
  * The documentation includes links to all existing Tutorials and Examples. Also see next section
* [CNTK Managed API](https://github.com/microsoft/cntk/wiki/CNTK-Library-Managed-API)
  * [CNTK Eval Examples](https://github.com/microsoft/cntk/wiki/CNTK-Eval-Examples)


### Python Examples and Tutorials (Jupyter Notebooks)

Recognizing the importance of Python in Deep Learning we have published (a constantly growing) set of Python Examples and Tutorials (the latter are implemented as Jupyter Notebooks). You will find all information at these locations:

* [Python Examples](https://cntk.ai/pythondocs/examples.html)
* [Python Tutorials (Jupyter Notebooks)](https://cntk.ai/pythondocs/tutorials.html)

On Linux you easily can use our preconfigured [CNTK Docker Containers](https://github.com/Microsoft/CNTK/wiki/CNTK-Docker-Containers#using-docker-container-to-run-cntk-jupyter-notebook-tutorials) to run CNTK Jupyter Notebooks.

### CNTK Evaluation library

The CNTK Library API allows to evaluate both CNTK model-v1 and model-V2 format.

In CNTK 2.0 the Evaluation Library can be used on Windows and Linux, in CPU and GPU configuration. C++, Python, as well as C# and other .NET languages are supported.

More informationSee more on [CNTK Evaluation Library here](https://github.com/Microsoft/CNTK/wiki/CNTK-Library-Evaluation-Overview).

### CNTK new features

We have introduced a lot of new features during the Beta period. The list below highlights some of them:

* Support of [object recognition using Fast R-CNN](https://github.com/Microsoft/CNTK/wiki/Object-Detection-using-Fast-R-CNN) algorithm.
* Integration with [NVIDIA NCCL](https://github.com/NVIDIA/nccl), a stand-alone library of standard collective communication routines, such as all-gather, reduce, broadcast, etc., that have been optimized to achieve high bandwidth over PCIe. See how to enable NCCL in the [CNTK Wiki](https://github.com/Microsoft/CNTK/wiki/Setup-CNTK-on-Linux#optional-nccl).
* Support of Asynchronous Stochastic Gradient Descent (ASGD)/Hogwild! training parallelization support using Microsoft’s Parameter Server ([Project Multiverso](https://github.com/Microsoft/multiverso)).
* Support of Distributed scenarios in Python API. See more in the sections on Distributed scenarios in [ConvNet](https://github.com/Microsoft/CNTK/blob/master/Examples/Image/Classification/ConvNet/Python/README.md) and [ResNet](https://github.com/Microsoft/CNTK/blob/master/Examples/Image/Classification/ResNet/Python/README.md) examples.
* Support for training on one-hot and sparse arrays via NumPy.
* Lambda rank and NDCG at 1 are accessible from Python for real this time.
* New Python and BrainScript for VGG16 and 19.
* [Performance Profiler for BrainScript and Python](https://github.com/Microsoft/CNTK/wiki/BrainScript-and-Python-Performance-Profiler).
* Support in training session for cross validation and preservation of all checkpoints.
* Ability to write your own optimizer in Python by inheriting from `UserLearner` and overriding the update method.
* Ability to implement Learners in Python using `UserLearner` [Read more here](https://www.cntk.ai/pythondocs/extend.html#user-learners).
* All deserializers are exposed in C++.
  * HTK deserializers are also exposed in Python.
* Support for TensorBoard output in both Python and BrainScript. [Read more here](https://github.com/Microsoft/CNTK/wiki/Using-TensorBoard-for-Visualization).
* Support for Model debugging in Python, that can be done conveniently similarly to gdb/pdb, by wrapping the model with `debug_model()` and training/evaluating it. [Read more here](https://www.cntk.ai/pythondocs/cntk.debugging.html#module-cntk.debugging.debug).

We have also implemented significant performance improvements.

## CNTK Installation and Usage
### New automated installation procedures

We have enabled different ways to install CNTK in an automated manner: 

* Installation scripts for binary distribution.
* Installation scripts for the users who would like to work with CNTK source code.
* Installation via `pip install` procedure.

Read more about [different ways to install CNTK here](https://github.com/Microsoft/CNTK/wiki/Setup-CNTK-on-your-machine).

### CNTK at Docker Hub and as self-built Docker Images

CNTK is now available as [Docker Images at Docker Hub](https://hub.docker.com/r/microsoft/cntk/).

You may also build your own Docker Images using pre-configured Docker files from CNTK Code base. See this [Wiki page on using CNTK as Docker Images and Containers](https://github.com/Microsoft/CNTK/wiki/CNTK-Docker-Containers).
 
### CNTK as NuGet packages

Windows developers using C++ and C# / .NET are welcome to use multiple CNTK NuGet packages supporting both v.1 and v.2 model formats.

See more on [CNTK NuGet packages here](https://github.com/Microsoft/CNTK/wiki/NuGet-Package).
