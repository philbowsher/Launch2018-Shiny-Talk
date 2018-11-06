# Launch2018 Shiny Talk - Nov 2018

The material in the repo supports a presentation given in November 2018.

Live PResentation is here:

http://colorado.rstudio.com:3939/content/1615/


## Part 1: Introduction to Shiny

To begin, we'll work with the openFDA API to explore adverse event data.

`01-adverse-events-plots.R` - This file includes our code to query the API and generate a few static plots.

`02-adverse-events.Rmd` - This file takes the same code snippets, but incorporates them into a HTML dashboard using the [flexdashboard](https://rstudio.github.io/flexdashboard) package. Markdown syntax is used to layout the plots into a dashboard. The R Markdown document includes a parameter, `params$drug`, so that different versions of the dashboard can easily be created for different drugs.

Here , we will pull in normalized names for clinical drugs.

https://www.nlm.nih.gov/research/umls/rxnorm/

`03-adverse-events-shiny.Rmd` - This file builds off the flexdashboard and adds `runtime:shiny` to turn the static HTML file into an intereactive Shiny application. The shiny application makes it easy to explore the affect of age on the distribution of adverse events. Notice the minimal code changes required to turn the document into an app!

Lastly, we will investigate Immunogenicity data with AEs, where the date are in a database.

We'll take a brief look at a version of the adverse events report that can be scheduled and emails out a PPT presentation. See https://github.com/sol-eng/adverse-events to view the full code. This type of scheduled report helps after stakeholders have played with a Shiny app and ask for "regular updates".

 We'll also look at the new [shinyreactlog](https://github.com/rstudio/shinyreactlog). 

The code for this application is available [here](https://github.com/jcheng5/rpharma-demo).

