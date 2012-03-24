knitcitations
=============

- **Author**: [Carl Boettiger](http://www.carlboettiger.info/)
- **License**: [CC0](http://creativecommons.org/publicdomain/zero/1.0/)
- [Package source code on Github](https://github.com/cboettig/knitcitations)
- [Online package documentation](http://cboettig.github.com/knitcitations/index.html)


`knitcitations` is an R package designed to add dynamic citations to dynamic documents created with [Yihui's knitr package](https://github.com/yihui/knitr).



Installation 
------------

Install directly from Github using [Hadley's devtools package](https://github.com/hadley/devtools)

```r
library(devtools)
install_github("knitcitations", "cboettig")
library(knitcitations)
````

You can also clone or download the repository and install with `R CMD INSTALL`. Once I'm through the early development phase a copy will be available on CRAN.


Quick start
-----------




Cite an article by DOI.  The full citation information is gathered automatically.



```r
citep("10.1890/11-0011.1")
```

 "(Abrams _et. al._ 2012)"



A key in the format `LastNameYear` is automatically created for this citation, so we can use it again without remembering the DOI.   



```r
citep("Abrams2012")
```

 "(Abrams _et. al._ 2012)"



(A custom key can also be given by naming the DOI, such as `citep(c(AbramsEtAl="10.1890/11-0011.1"))`).


Generate the final bibliography



```r
print(bibliography(), "html")
```

<p>Abrams PA, Ruokolainen L, Shuter BJ and Mccann KS (2012).
&ldquo;Harvesting Creates Ecological Traps: Consequences of Invisible Mortality Risks in Predator–Prey Metacommunities.&rdquo;
<EM>Ecology</EM>, <B>93</B>.
ISSN 0012-9658, <a href="http://dx.doi.org/10.1890/11-0011.1">http://dx.doi.org/10.1890/11-0011.1</a>.




Generate and use Bibtex files and more.  [See the full tutorial](https://github.com/cboettig/knitcitations/blob/master/inst/examples/citations.md).  
