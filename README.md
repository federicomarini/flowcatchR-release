flowcatchR
==========
[![Build Status](https://travis-ci.org/federicomarini/flowcatchR.png?branch=master)](https://travis-ci.org/federicomarini/flowcatchR)

#### A framework for tracking and analyzing flowing blood cells in time lapse microscopy images

**flowcatchR** is a set of tools to analyze in vivo microscopy imaging data, focused on tracking flowing blood cells.
It guides throughout all the steps of bioimage processing, from segmentation to calculation of features, filtering 
out particles not of interest, providing also a set of utilities to help checking the quality of the performed 
operations. The main novel contribution investigates the issue of tracking flowing cells such as the ones in blood
vessels, to categorize the particles in flowing, rolling and adherent by providing a comprehensive analysis of the
identified trajectories. The extracted information is then applied in the study of phenomena such as hemostasis and
study of thrombosis development. We expect this package to be potentially applied to a variety of essays, 
covering a wide range of applications founded on time-lapse microscopy.


### Installation
To install the development version for the package **flowcatchR**, please start a current version of R and type (using `devtools`):

```r 
# currently this can be done via github
install.packages("devtools") # if needed
devtools::install_github("flowcatchR", "federicomarini")
```

If you want to install the current release version, just type:
```r
source("http://bioconductor.org/biocLite.R")
biocLite("flowcatchR")
```



If required, install the dependencies:

```r
source("http://bioconductor.org/biocLite.R")
biocLite(c("EBImage","BiocStyle","BiocParallel"))

install.packages(c("rgl","colorRamps","knitr"))
```

### flowcatchR in a glimpse

```r
library("flowcatchR")
data("MesenteriumSubset")
fullResults <- kinematics(trajectories(particles(channel.Frames(MesenteriumSubset,"red"))))
```



### Vignette

To inspect the vignette and the code used in it, type:

```r
vignette("flowcatchR-vignette")
## and/or
browseVignettes("flowcatchR")
```

### Contact
For additional details regarding the functions of **flowcatchR**, please consult the documentation or write an email to marinif@uni-mainz.de. 

### Bug reports/Issues/New features

Please use https://github.com/federicomarini/flowcatchR/issues for reporting bugs, issues or for suggesting new features to be implemented.

