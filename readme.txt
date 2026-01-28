b/c the publication from RStudio is failing (see below), now using GitHub integration to render the _book/ contents after pushing to GitHub, rather than through RStudio bookdown::publish_book()
more details here and here 
 
- [ ] New URL: https://bansell-wehi-tidyr-course-book.share.connect.posit.cloud/ 

Bookdown.org decommissioned (website will go down end of 2027). Primary task to get book rendering w/o error and pushed to posit cloud as per https://pkgs.rstudio.com/bookdown/articles/bookdown-org-migration-guide.html
To render book (didn’t use R Projects) requires mkdir ~/Desktop/WEHI_tidyR_course/ and copy in data files

Posit publishing failing; #bookdown_retry  
unlink("rsconnect", recursive = TRUE)  # removes local deploy records
rsconnect::connectCloudUser()          # re-auth to Connect Cloud
bookdown::publish_book(render = "local")
