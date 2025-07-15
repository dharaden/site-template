# Website Template

Here is a brief walkthrough of things to update in order to have your website appear. 

# The Template Repository

When creating a project from this template, be sure to check "Include all branches". This will copy in the additional branches that are necessary to publish your site more easily.

There should be 3 different branches
1. main (default)
2. gh-pages
3. github-action

Remember that the name of the repository will be your pages URL
e.g. dharaden.github.io/site-template

## After Creating your own repository

### Step 1: Allow GitHub Action to render website
- Navigate to the current repo and select settings
- Settings > Actions > General
- Scroll down to "Workflow permissions"
-  Make sure "Read and write permissions" is selected (this gives the github-actions[bot] permission to push)

### Step 2: Check Pages
This should already be set up and your site will likely have already been published, but this is good to double check. 

- Settings > Pages 
    - Source should "Deploy from a branch"
    - The branch selected is "gh-pages" and the "/(root)" folder

This will use GitHub Actions to basically create an R environment and render all of your code to create the appropriate files for publishing the website.  

# Using the template

There are a lot of different ways to use this repository with countless tempaltes. Here are just a few things to help guide and some additional resources. 

## The R Environment
As stated above, the GitHub Actions creates an R environment to run the code. Therefore, we need to make sure that all libraries are installed into this since it is a new instance each time. 

We use the package `renv` to help out with keeping everything synced between the R-Studio that you work on and the R code that gets run through GitHub. 

Here is the website for `renv`: https://rstudio.github.io/renv/articles/renv.html

### Installing a new package 
Whenever you need to install a new package to use on your site, be sure to take a snapshot of the current installed packages using `renv::snapshot()`


## Website Structure
Each page on your website can be represented by different QMD files. 
