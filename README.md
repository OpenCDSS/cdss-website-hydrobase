# cdss-website-hydrobase #

This repository contains the content for the HydroBase local attachment instructions. 

* [Repository Contents](#repository-contents)
* [Development Environment](#development-environment)
* [Editing and Viewing Content](#editing-and-viewing-content)
* [Deploying the Website](#deploying-the-website)
* [License](#license)
* [Contributing](#contributing)
* [Maintainers](#maintainers)
* [Contributors](#contributors)
* [Release Notes](#release-notes)

------------------

## Repository Contents ##

The repository contains the following:

```text
cdss-website-hydrobase/  Repository name and main folder.
  .github/              Files specific to GitHub such as issue template.
  .gitattributes        Typical Git configuration file.
  .gitignore            Typical Git configuration file.
  README.md             This file.
  build-util/           Useful scripts to view, build, and deploy documentation.
  mkdocs-project/       Typical MkDocs project for this documentation.
    mkdocs.yml          MkDocs configuration file for website.
    docs/               Folder containing source Markdown and other files for website.
    site/               Folder created by MkDocs containing the static website - ignored using .gitignore.

```
A recommended but not required folder structure to contain the repository files on the local computer is:

```
C:\Users\user\                  Windows user files.
  cdss-dev/                     CDSS development files.
    Website-HydroBase/          This product.
      git-repos/                Git repositories for the website.
        cdss-website-hydrobase/ The repository files, as shown above.
```

## Development Environment ##

The development environment for contributing to this project requires installation of Python, MkDocs, and Material MkDocs theme.
Python 2 has been used for development but MkDocs with Python 3 is known to also work.
See [OWF / Learn MkDocs](http://learn.openwaterfoundation.org/owf-learn-mkdocs/) for information about MkDocs.

## Editing and Viewing Content ##

If the development environment is properly configured, edit and view content as follows:

1. Edit content in the `mkdocs-project/docs` folder and update `mkdocs-project/mkdocs.yml` as appropriate.
2. Run the `build-util/run-mkdocs-serve-8000.sh` script in Cygwin, Linux, Git Bash, or equivalent.
3. View contents in a web browser using URL `http://localhost:8000`.

The above process could be adapted to use a Windows batch files if necessary.

## Deploying the Website ##

The deployment process will be changed when the State has identified where the documentation can live within the CDSS website.

## License ##

The license for this documentation is being determined.
The Open Water Foundation consulting team has recommended using the [Creative Commons Attribution 4-0 Generic (CC BY 4.0) License](https://creativecommons.org/licenses/by/4.0/).

## Contributing ##

It is expected that most contributions to this project will be made by core OpenCDSS contributors,
in order to align OpenCDSS with State of Colorado programs.
However, suggestions are welcome and will be considered.
Contribute to the documentation as follows:

1. Use GitHub repository issues to report minor issues and maintainers will respond.
2. Use GitHub pull requests.

## Maintainers ##

This repository is maintained by the OpenCDSS team.

## Release Notes ##

The following release notes indicate the update history for major milestones. Refer to the repository issues page for incremental changes. 

* 2019-04-12 - initial version
