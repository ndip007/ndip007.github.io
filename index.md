## Project abstract

Support a continuous integration (CI) generation of SPDX files by creating a plugins or extensions to build tools. These plugins or extensions will generate valid SPDX documents based on the build file metadata and source files. 
The Yocto build environment currently has some SPDX file generation capabilities, but there is a need for some additional work to integrate some of the existing tools into a more complete integrated toolset. The SPDX Maven Plugin is an example of an existing build tool SPDX generator.

## Project goals

Write a build-tool agnostic plugin that can generate spdx file of an indicated project upon build.

This project is about the inclusion of high quality license information (for license compliance) to allow its use by downstream users of the code.
This is very important because many build environments do not always include license information in their metadata, and do not produce sufficient information for good license compliance.
THis project is generally about implementing a build tool spdx file generator plugin for build environments such as the following:
- MSBuild
- PIP
- NPM (Note: NPM does include SPDX compliance license information and tools)
- DEB

## Development constraints

The first two project types selected were:
- Python projects
- Node projects

And as build tool, the integration had to be done on travis-CI.

## Development modules

### Analyser module

This module is responsible for discovering which type of project we are dealing with; whether it is a Python or a node project. It contains a parser and a manager.
The manager class recieves a project directory as input and is responsible for getting which file to parse for dependencies.
The parser recieves a single package.json(in the case of a node project) file directory as input, and parses it to return the dependencies.

### Downloader module
The downloader module uses the input from the analyser module to download package dependencies into a temp directory.

### Scanner module
The scanner module is responsible for scanning the project being built using scancode-toolkit.

## How to test the plugin

### 1. Requirements.
Install python3 venv
`sudo apt-get install python3-venv`
Install python 3
`sudo apt-get update`
`sudo apt-get install python3`
`sudo apt-get install python3=3.5.1*`

### 2. Pull the project.
Pull the project into a folder say "spdx"

### 3. Create a virtual environment for the project.
In the folder "spdx", run the command `python3 -m venv .`.
This will create a virtual environment for the project.

### 4. Activate the virtual environment.
In the "spdx" folder, run `source bin/activate`.
This will activate the virtual environment for the project.

### 5. Install the project requirements.
Now run the command `pip install -r spdx-build-tool/requirements.txt`.

### 6. Install the project.
cd into the directory "build-tool", ie `cd spdx-build-tool`.
Run `pip install -e .`

### 7. The entry points.
There are several entry points, but the one that does the analysis, parsing and download is `spdx-build`.
So, Run `spdx-build '~/Desktop/(some-project)/'`.

## Future work scope

In the future, other project types will be included into this build tool; including the following:
- java projects
- ruby

Also, other build tools will be integrated:
- yocto
- DEB
- MSbuild, etc
