NHS data releases analysis
==========================

By [Max Harlow](https://twitter.com/maxharlow)


Data
----

Our source was the [NHS register of approved data releases](https://digital.nhs.uk/services/data-access-request-service-dars/register-of-approved-data-releases), which is published as a series of Excel files. The data runs from April 2016 through to May 2021. They have published data prior to this, going back to 2014, but they are in a different format and don't include some details, such as whether opt-outs were applied or not. From 2019 files have been published monthly. Each of these source files were extracted and combined.

* `nhs-data-release-register-releases.csv` is a combined list of all the data releases.

As well as this releases data, the source files include the purposes given by the recipient under which those agreements were made, which was used in our reporting. The files also have an amendments tab with corrections to previously published files listing releases that were omitted or mistated. Since these amendments mostly appear to have been added in to subsequent release files, they were not included in our analysis.

This data was joined with some additional information, which was produced largely manually:

* `date-ranges.csv` lists start and end dates for the periods each of the source files cover.
* `supplementary-names.csv` includes nicely-formatted organisation names and types for every organisation. For companies, where two have both recieved data have since merged the name of the merged entity is used. In cases where the company has since changed name the original name given is used.
* `supplementary-details.csv` includes further details and subtypes for selected organisations.


Analysis
--------

The data analysis for this story is in [`analysis.ipynb`](analysis.ipynb).
