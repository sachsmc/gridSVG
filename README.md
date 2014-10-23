gridSVG
=======

My version of gridSVG modified to work on shinyapps.io. The problem is with the `localeToCharset()` function, which returns NA on shinyapps.io. I have modified the single line below so that it works on shinyapps.io. 


      if(is.na(localeToCharset())) isUTF8 <- TRUE else isUTF8 <- localeToCharset()[1] == "UTF-8"
     
This is a hack, and is not expected to work in general.      

View the original [here](https://sjp.co.nz/projects/gridsvg/).
