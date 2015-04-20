# rkolada

Simple R package to access the Kolada API (http://www.kolada.se/).

    # devtools::install_github('reinholdsson/rkolada')
    library(rkolada)
    x <- rkolada()

## Get kpi:s

    x$kpi()  # all
    x$kpi('N00008')
    x$kpi(c('N00008', 'N00009))

## Get municipalities

    x$municipality()  # all
    x$municipality('1440')
    x$municipality(1440:1489)

## Get values

    x$values('N00006', '0764', 2000:2010)
    x$values('N00006', '0764', 2000:2010, all.cols = T)  # with extra kpi and municipality columns (meta data)
    x$values(c('N00006', 'N00007'))  # get all municipalites and years of both kpi:s
    