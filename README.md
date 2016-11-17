# Provenance Index CSV Exports

The J. Paul Getty Trust (the "Trust"), operating as the Getty Research Institute, has embarked on a three-year project to redesign the current infrastructure of the [Getty Provenance Index® databases](http://www.getty.edu/research/tools/provenance/) and publish them as Linked Open Data (LOD). 
Because this is a time-consuming process, we want to enable open and convenient access to full datasets from the Getty Provenance Index® for researchers during early stages of this project, before the LOD versions are released to the public.

**These data will eventually be superseded by the Linked Open Data release.**
While this repository will remain public after the LOD release, the datasets it contains will not be maintained in any way.
When a dataset published in this repository is replaced by its continuously maintained LOD version, it will be switched from "Active" to "Unsupported" in the table below.

|Knoedler|[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)|

## Repository structure

The Getty Provenance Index® comprises several distinct databases. 
The quantity and scope of research material that is available in each database varies by region, period, and type of document.

Each database is provided in one or more CSV (comma separated values) files in its own directory. Each of these directories contains a database-specific README file documenting the sources from which each dataset has been derived, as well as a data dictionary with a description of each table column. 
You can view these database-specific files online by clicking on the respective directories listed above.

## Usage guidelines

### License

The Trust makes the Getty Provenance Index® datasets available under the least restrictive open license possible; however, **please check the README documentation specific to each dataset, as rights may vary between datasets**.
If you create a derivative dataset from a Getty Provenance Index® dataset, we ask that you consider releasing the derivative under the least restrictive license possible.

### Attribution

We respectfully ask that you acknowledge the Getty Research Institute® and Getty Provenance Index® as sources wherever possible, in order to preserve links to the datasets. By providing acknowledgment or citation, you enable others to verify, replicate, and further explore your presentation and interpretation of our data.

Suggested citation:

Getty Research Institute®, _CSV exports of the Getty Provenance Index®__ (November 17th, 2016), <https://github.com/gettydata/releases/tag/v1>

Note that a new tagged release will be made whenever any of these datasets are added or updated. A list of these tagged releases can be seen here: <https://github.com/gettydata/releases>

### Data Integrity/DISCLAIMER OF WARRANTIES

These data are provided for the purposes of exploration, education, experimentation, and fun, but are to be used at your own risk. 
The Trust shall not be held liable for any improper or incorrect use of the information contained herein and assumes no responsibility for anyone's use of the information.

The Getty Provenance Index® databases are regularly updated by editors to reflect our latest research. 
The most current data are available via the Getty Provenance Index® search interface (see <http://www.getty.edu/research/tools/provenance/search.html>).
Updates to the datasets in this repository are not scheduled but may occur.
You are advised to use, or update to, the most current version of these datasets for best accuracy.

No warranty, express or implied, is made regarding accuracy, adequacy, completeness, legality, reliability or usefulness of any information provided.
The Trust provides this information on an "AS IS" basis.
All warranties of any kind, express or implied, including but not limited to the IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, freedom from contamination by computer viruses and non-infringement of proprietary rights ARE DISCLAIMED to the maximum extent permitted by law.

### Trademark Policy/No Endorsement

Use of these datasets does not grant or imply the Trust's approval, commission, or support of your work. 
The names "Getty®, "The Getty®, "The Getty Research Institute®" and "The Getty Provenance Index®" are registered trademarks of the Trust, and are not part of the datasets. 
If you transform or modify a dataset, you must clearly distinguish the resulting work as having been modified from the Getty Provenance Index® dataset and may not imply any endorsement by the Trust.

### Pull Requests, Issues, and Bug Reports

Please note that, as these data are exported from our internal databases, we cannot accept pull requests for the data in this repository. 
However, during the period when this repository is actively maintained (before the LOD release), we will review issues and pull requests for documentation or other non-data content issues posted here.

### Acknowledgment

This repository and README are largely inspired by the detailed work done by the [Carnegie Museum of Art](https://github.com/cmoa/collection) on their own collections data repository.
We thank them for providing an excellent model!
