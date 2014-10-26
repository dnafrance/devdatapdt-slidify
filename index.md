---
title       : Simple Interest Calculator
subtitle    : RStudio Shiny application
author      : dnafrance
job         : Course Project in "Coursera - Developing Data Products"
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction
This is an RStudio shiny application developed as a course project for Coursera's **Developing Data Products** course in the *Data Science Specialization* track.  
  
The application developed is a **simple interest calculator**.  
  

### Course project requirements
The course project requirements for this application are:
* Some form of input (widget: textbox, radio button, checkbox, ...)
* Some operation on the ui input in sever.R
* Some reactive output displayed as a result of server calculations
* You must also include enough documentation so that a novice user could use your application.
* The documentation should be at the Shiny website itself. Do not post to an external link.

--- .class #id 

## Application - Widgets
The shiny application for this project is a [simple interest calculator](https://dnafrance.shinyapps.io/devdatapdt/).  
It includes 4 widgets:  
  
1. **numericInput** - A field to enter numbers, in this case - the principal amount (in $)  
2. **sliderInput** - A slider bar
    + First slider is to choose the yearly interest rate (in %)
    + Second slider is to choose the number of time periods  
3. **selectInput** - A box with choices to select from, in this case - the type of time period: years, quarters or months  
4. **actionButton** - A Action Button, in this case to provide non-reactive reactivity to refresh and calculate

---

## Application - Operations and Output
To prevent undue distraction, the reactivity of the shiny application widgets is controlled by using an actionButton. Based on user inputs, and using the simple interest calculation equation, the application displays:  
1. Inputs entered by the user  
2. Calculated values  
 a. Simple interest calculated  
 b. Total amount calculated as principal plus interest  
  
The simple interest calculation equation is:  
**A = P + I = P(1 + rt) ; R = r * 100**  
where:  
A = Total amount (Principal + Interest), P = Principal amount, I = Interest amount, r = Rate of interest per year, in decimal; r=R/100, t = Time period invested in years/quarters/months    
  
Even though it is a simple application, to make it easy for the novice user, the **Documentation** tab in the mainPanel of the application lists the details of the calculation of simple interest.

---

## Application - Link and Code

Try out the application on the RStudio shinyapps.io website:  
https://dnafrance.shinyapps.io/devdatapdt/ 

To see the code for the application, visit github website:  
https://github.com/dnafrance/DevDataPdt  

Useful files in repo:  
* ```server.R```
* ```ui.R```
  
To execute the application and see the code in action, use:  
```runApp(displayMode = 'showcase')```






