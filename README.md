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

1. The website is deployed by running copy-to-co-dnr-gcp.sh in the build-util directory.
   This Shell Script is run in Git Bash by running the command "bash copy-to-co-dnr-gcp.sh". 
2. Running the script requires that gsutil is installed, which is part of the Google Cloud SDK: https://cloud.google.com/sdk/docs/
   When gsutil is installed, it will need to be authenticated with a Google login that has permissions to write to the DNR - OpenCDSS GCP bucket (below)
   https://console.cloud.google.com/storage/browser/opencdss.state.co.us?project=dnr-website-host-012639&orgonly=true&supportedpurview=organizationId
3. Within copy-to-co-dnr-gcp.sh, the variable gsFolder needs to be set to the correct bucket and folder. In this case gsFolder="gs://opencdss.state.co.us/hydrobase".
4. Once the script is run, the built MKDocs site should be transferred to the GCP bucket.
5. The website is created: http://opencdss.state.co.us/hydrobase/ or http://opencdss.state.co.us/hydrobase/index.html.


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
