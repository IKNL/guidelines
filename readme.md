# Guidelines
This repository is to give some guidelines regarding documenting, naming and ordering conventions for ppDLI repositories and releases.

## 1. Repositories

* Repository names should be snake_case (underscores between words) and consist only off small letters
* In case of an algorithm it should start with a "d" (e.g. d_summary)
* Should always contain a read me (see section bellow)
* Preferable Algorithm regpositories start from the boilerplate (link)[link]

## 2. Readme 

### 2.1 Algorithm ReadMe

* Short description of what the algorithm does do (preferable with an image)
* A link to the registry where the image is stored (e.g. https://docker-registry.distributedlearning.ai/d_summary)
* It should contain the banner that it is part of the ppDLI
* It should contain a link to our webpage https://distributedlearning.ai
* A reference to the documentation https://docs.distributedlearning.ai
* It should mention the current status of the algorithm
* It should explain how to test the image locally
* It should mention the current status of the algorithm
    * Broken
    * Alpha
    * Beta
    * Prod

### 2.2 Other ReadMe

* It should contain the banner that it is part of the ppDLI
* It should contain a link to our webpage https://distributedlearning.ai

## 3. Docker Registry

* The image name should be identical to the repository name
* Algorithms are seperated in development stage / (e.g. https://docker-registry.distributedlearning.ai/prod/d_summary)
    * alpha (only for internal use)
    * beta (use with caughtion)
    * prod (battle tested)
* Infrastructure images go in the folder /infrastructure (e.g. https://docker-registry.distributedlearning.ai/infrastructre/node)

## 4. Versioning

* We follow the PEP 440 (link)[https://www.python.org/dev/peps/pep-0440/]
* breaking.major.minor.label. Labels could be .postN, which indicates that is a post release, or .devN, that indicates that this is a development version (pre-release)
* The latest release should always consist of the code at the master branch
* We use the github-releases 
* In case it is release on pipy, it should maintain the same version number






