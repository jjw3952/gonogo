# gonogo
gonogo provides sensitivity testing practitioners and researchers
with an ability to conduct, analyze, and simulate various sensitivity experiments 
involving binary responses and a single stimulus level (e.g. drug dosage, drop height,
velocity, etc.). Included are the modern Neyer and 3pod adaptive procedures, as well as
the Bruceton and Langlie. The latter two benchmark procedures are capable of being
performed according to generalized up-down transformed-response rules. Each procedure
is designated phase-one of a three-phase experiment. The goal of phase-one is to
achieve overlapping data. The two additional (and optional) refinement phases utilize
the D-optimal criteria and the Robbins-Monro-Joseph procedure. The goals of the two
refinement phases are to situate testing in the vicinity of the median and tails of the 
latent response distribution, respectively.

## Installation

gonogo runs on R, which is a statistical computing package. This repository has packaged 
the gonogo software as an R package so that it can be readily installed and updated.

Although R is a powerful tool, there is a learning curve. The good news is that you don't
need to know much about R to use gonogo.

You'll need to install R and RStudio. The following instructions assume that you are
using Windows. 

[R](https://cran.rstudio.com) has the core features. You'll need a recent version, 
preferably version 4 or later. Click on “Download R for Windows”, then click on “base”, 
then click on “Download R [version number] for Windows”. Install the downloaded file. 

[RStudio](https://rstudio.com/products/rstudio/download/#download) is the user interface
that provides convenient access to R and all related features. You'll need a recent version,
preferably version 1.4 or later. Download and install the version for Windows 10/8/7. 

Once R and RStudio are installed, launch RStudio. To install (or re-install) this package,
type the following into the Console window at the lower left:

    install.packages("devtools")
    library(devtools)
    install_github("joncutting/gonogo")
    
If you get a message about "Do you want to install from sources the package which needs 
compilation", click No.
    
## Usage

To use gonogo, start RStudio and type the following into the Console window at the lower left:

    library(gonogo)

Now you have the gonogo functions available for use, for example:

    z=gonogo(mlo=0,mhi=22,sg=3,reso=0.01,term1=F)
    ptest(z,3)

Full documentation about the use of gonogo functions is available at [Gonogo: An R Implementation of Test Methods to Perform, Analyze and Simulate Sensitivity Experiments](https://arxiv.org/abs/2011.11177).

## Development

If you would like to contribute content to the gonogo package, you will need a few
additional tools on your computer. In addition to R and RStudio, you will need
to install Rtools.

[Rtools](https://cran.r-project.org/bin/windows/Rtools/) is a collection of tools required
to compile R code. To install Rtools, download and install the Windows 64-bit version
from the link above. Be sure to add Rtools to your PATH environment variable.

For information on the structure of an R package, please refer to the document [Writing R Extensions](https://cran.r-project.org/doc/manuals/r-release/R-exts.html).

## Credits

The original gonogo software and accompanying documentation were written by Paul A. Roediger while
working as a contractor for the US Army ARDEC at Picatinny, New Jersey, USA. That work was approved 
for public release and for unlimited distribution. 

## References

Ray, D. M., & Roediger, P. A. (2018). Adaptive testing of DoD systems with binary response. CHANCE, 31(2), 30-37.

Roediger, P. A. (2020). Gonogo: An R Implementation of Test Methods to Perform, Analyze and Simulate Sensitivity Experiments. arXiv preprint arXiv:2011.11177.

Wang, D., Tian, Y., & Jeff Wu, C. F. (2020). Comprehensive comparisons of major sequential design procedures for sensitivity testing. Journal of Quality Technology, 52(2), 155-167.

Wu, C. J., & Tian, Y. (2014). Three-phase optimal design of sensitivity experiments. Journal of Statistical Planning and Inference, 149, 1-15.
