## Test environments
* local OS X install, R 3.6.1
* ubuntu 14.04 (on travis-ci), R 3.6.1
* win-builder (devel and release)

## R CMD check results

There were no ERRORs, or WARNINGs.

There were 2 NOTEs:

  * Note 1: Checking CRAN incoming feasibility ... NOTE
  Maintainer: 'Luis F. Duque <lfduquey@gmail.com>'
  
  According to CRAN Maintainer Uwe Ligges, "This is just a note that reminds CRAN maintainers to check that the              submission comes actually from his maintainer and not anybody else." Thus, it can be considered a harmless note.

  * Note 2: checking top-level files ... NOTE
  Files 'README.md' or 'NEWS.md' cannot be checked without 'pandoc' being installed.
  
  It is a harmless note. If I add the README.md file to .Rbuildignore, this note will disappear, but I prefer to leave       it. 

### Submission comments 

02-03-2020 This is a new submission. In this version I have:

* Used "\donttest{}" for the example of the drawre function. The run time of this 
  example depend on the number of cores of the computer; it can be greater than 5 seconds.
  This function is limited to using a number of cores <=2.
