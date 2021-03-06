<img src="https://github.com/IKNL/guidelines/blob/master/resources/logos/iknl_nl.png?raw=true" width=200 align="right">

# Guidelines
This repository is to give some guidelines regarding documenting, naming, and version conventions for IKNL repositories and releases.

## 1. Repositories

* Repository names should be `snake_case` (underscores between words) and consist only of small letters
* In case of a federated learning algorithm, it should start with a "d" (e.g. d_summary)
* In case it is an demo algorithm, please add the `_test` suffix
* Should always contain a `README.md` (see section bellow)
* Preferable Algorithm repositories start from the [boilerplate](https://github.com/IKNL/d_boilerplate)

## 2. Readme
[READMEs are important](https://www.makeareadme.com/). Therefore, each repository should have one and include:
* A short description of what the algorithm does do (preferable with an image)


### 2.1 Federated Learning Algorithm
* VANTAGE6's logo. Just make the following the first line of your README:

`<img src="https://github.com/IKNL/guidelines/blob/master/resources/logos/vantage6.png?raw=true" width=200 align="right">`

* In the README, use the following text as an introduction to the description of the repository:

> Federated learning (FL, also known as distributed learning) algorithms try to learn a global model using data from different sources without data ever leaving their original location. Furthermore, no raw (patient) sensitive data are shared between any of the parties. In other words, instead of bringing the data to the algorithms, we bring the algorithms to the data.
> 
> In this repository, we provide a FL implementation of...

* The banner that indicates that it is part of VANTAGE6:

|:warning: priVAcy preserviNg federaTed leArninG infrastructurE for Secure Insight eXchange (VANTAGE6) |
|------------------|
| This algorithm is part of [VANTAGE6](https://github.com/IKNL/VANTAGE6). A docker build of this algorithm can be obtained from __docker-registry.distributedlearning.ai/d_summary__ |

* A link to the registry where the image is stored (e.g., https://docker-registry.distributedlearning.ai/d_summary)
* A reference to VANTAGE6's technical paper (WIP)
* A reference to the documentation https://docs.distributedlearning.ai
* A link to our webpage https://vantage6.ai
* The current status of the algorithm
* An explanation of how to test the image locally
* The current status of the algorithm
    * Broken
    * Alpha
    * Beta
    * Prod

### 2.2 Other Algorithms
* IKNL's logo (just like this one). Just make the following the first line of your README:

`<img src="https://github.com/IKNL/guidelines/blob/master/resources/logos/iknl_nl.png?raw=true" width=200 align="right">`


### 2.3 Other READMEs
<!---
* It should contain the banner that it is part of VANTAGE6
* It should contain a link to our webpage https://distributedlearning.ai
-->
## 3. Docker Registry (only for VANTAGE6 and Algorithms)

* The image name should be identical to the repository name
* Algorithms are separated in development stage / (e.g., https://docker-registry.distributedlearning.ai/prod/d_summary)
    * alpha (only for internal use)
    * beta (use with caution)
    * prod (battle tested)
* Infrastructure images go in the folder /infrastructure (e.g. https://docker-registry.distributedlearning.ai/infrastructre/node)

## 4. Versioning

* We follow the [PEP 440](https://www.python.org/dev/peps/pep-0440/)
* breaking.major.minor\[.label\] Labels could be .postN, which indicates that is a post release, or .devN, that indicates that this is a development version (pre-release)
* The latest release should always consist of the code at the master branch
* We use github-releases
* In case it is released on pipy, it should maintain the same version number
