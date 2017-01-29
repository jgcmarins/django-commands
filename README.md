# django-commands
A repository that provides information about on how to develop web apps with django.

## Index
- [Index](#index)
- [Description](#description)
- [Setup](#setup)
	- [venv](#venv)
		- [Activation](#activation)
		- [Deactivation](#deactivation)
- [Installation](#installation)
- [TODO](#todo)
- [Contribution](#contribution)
- [License](#license)

## Description
<p align="left">
When we work with frameworks, there are some basic rules that we may need to follow. The purpose of this repository is to help me and anyone else to keep the right way when starting a new django project.
</p>

## Setup
<p align="left">
First things first. Let's setup our work environment.</p>
<p align="left">
So, a good pratice, is to create our project inside a virtual environment. Why? Doing this, we protect all projects from each other. In other words, each django project can have its own independent set of installed packages.
</p>

#### venv
Python's official library that provides this tool is [venv](https://docs.python.org/3/library/venv.html).
To create a virtual environmet, type:

```
python3 -m venv /path/to/new/virtual/environment
```

###### Activation
Now that we have created our virtual environment, let's active it:

```
source <venv>/bin/activate
```

Where *<venv>* is the */path/to/new/virtual/environment*.

###### Deactivation
To deactive, just type:

```
deactivate
```

## Installation
Alright, now that we have our work environment, let's install django ~~finally~~. Remember: with virtual environment active, everything we install, will be installed inside our virtual environment.

## Contribution
<p align="left">
I am still learning django so, please, if you find any wrong information, submit an issue or create a pull request. Thanks! :octocat:
</p>

## License
[GPL-3.0](/LICENSE)
