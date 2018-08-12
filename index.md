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

## How to test plugin

## Future work scope




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/ndip007/ndip007.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ndip007/ndip007.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
