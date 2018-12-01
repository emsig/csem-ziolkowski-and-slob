# Numerical Examples of Ziolkowski and Slob (2019)

[![DOI](https://zenodo.org/badge/119286845.svg)](https://zenodo.org/badge/latestdoi/119286845)

The notebooks in this repository reproduce the numerical examples given in
Chapter 5 of the following book:

- - -

### Introduction to Controlled-Source Electromagnetic Methods: Detecting Subsurface Fluids
Anton Ziolkowski and Evert Slob, 2019, *Cambridge University Press*,
ISBN: [9781107058620](https://www.cambridge.org/9781107058620).

#### Abstract

*This volume describes how controlled-source electromagnetic methods are used
to determine the electrical conductivity and hydrocarbon content of the upper
few kilometres of the earth, on land and at sea. The authors show how the
signal-to-noise ratio of the measured data may be maximised via suitable choice
of acquisition and processing parameters and selection of subsequent data
analysis procedures. Complete impulse responses for every electric and magnetic
source and receiver configuration are derived, providing a guide to the
expected response for real data. One-, two- and three-dimensional modelling and
inversion procedures for recovery of earth conductivity are presented,
emphasising the importance of updating model parameters using complementary
geophysical data and rock physics relations. Requiring no specialist prior
knowledge of electromagnetic theory, and providing a step-by-step guide through
the necessary mathematics, this book provides an accessible introduction for
advanced students, researchers and industry practitioners in exploration
geoscience and petroleum engineering.*

- - -

The original figures in the book were created by Evert Slob in Matlab, using
the formulae as given in the book. The figures presented here are reproductions
using the Python modeller [empymod](https://empymod.github.io) ([Werthmüller,
2017](http://doi.org/10.1190/geo2016-0626.1)), which uses the derivations as
given in [Hunziker et al. (2015)](http://doi.org/10.1190/geo2013-0411.1) and
[Slob et al. (2010)](http://doi.org/10.2528/PIER10052807). Both solutions are
exact in the wavenumber-frequency domain, and for the diffusive half-space
solution also in the space-frequency and space-time domains, so the results
have to be the same up to numerical precision and differences in the Hankel-
and Fourier-transforms. We compared the results from the Matlab scripts and the
Python code to ensure that they agree<sup>&dagger;</sup>. This is particularly
valuable as the formulation of the book and the formulation on which empymod is
based upon are not exactly the same. Whilst the numerical results are the same,
their appearance might slightly differ due to the use of different plotting
libraries (Matlab vs. Matplotlib).

<sup>&dagger;</sup>Exceptions occur in examples that have added random noise
and also in examples which show the relative error, where tiny differences can
blow up quite significantly in the relative error when the responses go to
zero.


## Installation & requirements

The notebooks require at least `empymod v1.7.1`. The version included in the
zip-archive of CUP is `empymod v1.8.1`.

### Requirements

Python 3.5+ and recent versions of `NumPy`, `SciPy`, `matplotlib`, `IPython`,
and `Jupyter`.

If you are new to Python I recommend using a Python distribution, which will
ensure that all dependencies are met, specifically properly compiled versions
of NumPy and SciPy; my preferred option is the
[Anaconda](https://www.anaconda.com/download) distribution.


### Using the zip-archive provided by CUP

The zip-file is available as an *Online Resource* to the book at
[cambridge.org/csem](https://www.cambridge.org/csem).

Make sure your installation of Python meets the requirements. Then simply
extract the archive and open the notebooks with your installation of Jupyter.
The source code of empymod is located in the same folder, so Python will find
it automatically.


### Using the newest versions of the notebooks and empymod

Make sure your installation of Python meets the requirements. Follow the
instructions on [empymod.github.io](https://empymod.github.io) to install the
newest version of empymod using `conda` or `pip`. The maintained versions of
the notebooks are available at
[github.com/empymod/csem-ziolkowski-and-slob](https://github.com/empymod/csem-ziolkowski-and-slob).


## References

> Hunziker, J., J. Thorbecke, and E. Slob, 2015, The electromagnetic response in
> a layered vertical transverse isotropic medium: A new look at an old problem:
> Geophysics, 80(1), F1-F18; DOI:
> [10.1190/geo2013-0411.1](http://doi.org/10.1190/geo2013-0411.1).
>  
> Slob, E., J. Hunziker, and W. A. Mulder, 2010, Green's tensors for the
> diffusive electric field in a VTI half-space: PIER, 107, 1-20: DOI:
> [10.2528/PIER10052807](http://doi.org/10.2528/PIER10052807).
>  
> Werthmüller, D., 2017, An open-source full 3D electromagnetic modeler for 1D
> VTI media in Python: empymod: Geophysics, 82(6), WB9-WB19; DOI:
> [10.1190/geo2016-0626.1](http://doi.org/10.1190/geo2016-0626.1).
>  
> Ziolkowski, A., and E. Slob, 2019, Introduction to Controlled-Source
> Electromagnetic Methods: Cambridge University Press; ISBN:
> [9781107058620](https://www.cambridge.org/9781107058620).


## License

Copyright 2018 Dieter Werthmüller

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
