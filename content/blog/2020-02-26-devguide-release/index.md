---
slug: "devguide-release"
title: 'rOpenSci Dev Guide 0.4.0: Updates'
authors:
  - Maëlle Salmon
  - Brooke Anderson
  - Anna Krystalli
  - Lincoln Mullen
  - Karthik Ram
  - Noam Ross
  - Scott Chamberlain
  - Melina Vidoni
date: 2020-02-26
categories: blog
topicid:
tags:
  - Software Peer Review
  - dev guide
description: "Updates in version 0.4.0 of the online book 'rOpenSci Packages: Development, Maintenance, and Peer Review
rOpenSci Packages: Development, Maintenance, and Peer Review'"
twitterImg: img/blog-images/2019-05-16-dev-guide-update/cover.png
---

## New security guidance

 add more guidance about secrets and package development in the security chapter.
 
 For further discussion on the same topic, see [this `vcr` issue about making tests pass in PRs in the absence of necessary secrets](https://github.com/ropensci/vcr/issues/137) 

## Policy and governance changes

### Policy changes

add field and laboratory reproducibility tools as a category in scope.

add guidance for off-thread interaction and COIs ([`@noamross`](https://github.com/noamross), #197).

### Submission form amendments

explicit mention of roxygen2. See https://yihui.org/rd2roxygen/

explicit mention of the packaging guide and guide for authors

explicit mention of Bioconductor like CRAN

### Editor guidance

rephrase the EiC role (#244). tl;dr editors trust the EiC and are busy. :-)
 
add more guidance for the editor in charge of a dev guide release (#196, #205).

add guidance in the editor guide about not transferred repositories.
 
### How (not) to acknowledge rOpenSci
 
 remove the recommendation to add rOpenSci footer (https://github.com/ropensci/software-review-meta/issues/79).

remove the recommendation to add a review mention to DESCRIPTION but recommends mentioning the package version when reviewers are added as "rev" authors.


## Package documentation

### Documentation 

add note in Documentation sub-section of Packaging Guide section about referencing the new R6 support in roxygen2 (ropensci/dev_guide#189)

slightly changes the advice on documentation re-use: add a con; mention `@includeRmd` and `@example`; correct the location of Rmd fragments (#230).

### Documentation website

improve guidance regarding the replacement of "older" pkgdown website links and source (#241, [`@cboettig`](https://github.com/cboettig))

add package logo guidance (#217).

mention an approach for pre-computing vignettes so that the pkgdown website might get build on rOpenSci docs server.

document the use of mathjax with rotemplate ([`@Bisaloo`](https://github.com/Bisaloo), #199).

## Misc

### CRAN gotchas

Quite cool that those were contributed by package authors to lessen the probability of other authors' mixing the policies.

add one CRAN gotcha: single quoting software names(#245, [`@aaronwolen`](https://github.com/aaronwolen))

add new CRAN gotcha about having 'in R' or 'with R' in your package title ([`@bisaloo`](https://github.com/Bisaloo), ropensci/dev_guide#221)

### Forum guidance

clarify forum guidance (for use cases and in general).


### Package dependencies

add advice on specifying dependency minimum versions ([`@karthik`](https://github.com/karthik), [`@annakrystalli`](https://github.com/annakrystalli), #185).

Bioconductor
 
## Meta: changes in deployment

### GitHub actions

start using GitHub actions instead of Travis for deployment.

 hvitfeldt.me/blog/bookdown-netlify-github-actions (that I didn't use, but that is a very thorough walkthrough) and speakerdeck.com/jimhester/github-actions-for-r.
 
### URL checking

Mention the script checking URLs now use commonmark instead of regular expressions, and add a link to ropensci.org/technotes/2019/12/19/urls-tidying