## Project abstract

Support a continuous integration (CI) generation of SPDX files by creating a plugins or extensions to build tools. These plugins or extensions will generate valid SPDX documents based on the build file metadata and source files. 
The Yocto build environment currently has some SPDX file generation capabilities, but there is a need for some additional work to integrate some of the existing tools into a more complete integrated toolset. The SPDX Maven Plugin is an example of an existing build tool SPDX generator.

## Project goals

Write a build-tool agnostic plugin that can generate spdx file of an indicated project upon build.

## Development constraints

The first two project types selected were:
- Python projects
- Node projects

And as build tool, the integration had to be done on travis-CI.

## Development results

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
