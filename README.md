# Shiny-Rhino
You can start a Rhino project by running 
        rhino::init("my_app")

1. Rhino File Structure.
    Main Source Files
- app.R - 
- app - where the shiny application lives it contains
        - view - for shiny modules and related code 
        - logic - for application code independent of shiny
        - js - where the javascript files go into, with index.js as the entry point
        - styles - Sass code goes here and rhino sources the file for you. All you need to call is - - -    `rhino::build_sass()` function
        - static - Add static files here i.e. Images, favicons, and static files
        - main.R - Entry point for your application

- config.yml -is the configuration file for the rhino app

- tests - where to add unittests

- renv -
- renv.lock - take snapshots
- dependancies.r - add packages here


2. Code Architecture
- box i.e
        box::use(
            Shiny(Ns,moduleserver,Uioutput, renderUI))
- modules

3. Code Quality
    a. Linting - Refers to the process of analyzing code to detect potential errors, stylistic issues, and non-optimal coding practices.
            rhino::lint_r()
            rhino::lint_Sass()
            rhino::lint_js()
    b. Testing - Ensures that your app functions correctly and is reliable for its users.
            rhino::test_r()
            rhino::test_e2e()
    c. Logging - Critical aspect of software development and maintenance, providing a way to record events that happen during the execution of a program. 
            daroczig
            box::use(
                rhino(log),
            )
        
    d. Configuration - Configuration in the context of software development refers to the process and mechanism by which you define and manage the settings and parameters that influence the behavior of a software application.   
        - Store and retrieve variables from your shiny application i.e. 
                box::use(
                    config(get)
                )

