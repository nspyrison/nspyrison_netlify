# Nick's blogdown site, Academic template.

* Repo for hosting website, https://nspyrison.netlify.com


## Workflow/reminders

* blogdown::check_site(): a battery of checks and suggestions for cleanup.
* blogdown::build_site() (or Build tab > Build Website button): rebuilds the site content, to reflect any changes made to the files.
* blogdown::serve_site(): display the site content to Viewer panel/browser.

* cv/resume lives in ./static/media
* Content lives in ./content/authors/nicholas/_index.md
* Blog posts live in: ./content/post/, blog section will need to be turned on
* Author picture lives in ./content/authors/nicholas/avatar.jpeg
* /assets/: think of this as themeing and dependencies for the website itself, the tab icon exists in /assets/images/icon.png
* /static/: think of this as a /figures or /output folder; images, gif, and other files that are referenced in the /content/ section belong here.
* /content/: primary point of changes. Stores compilable files such as .md, .rmd.
* /public/: __Do not touch this!__; This is the content that is being hosted. blogdown::build_site() compiles the /content/ and overwrites the output to public for hosting.
* /config/_default/menus.toml: Changes the availablity on the burger menu, but not the contetnt itself.


## Resources:

* Academic Template for [Hugo](https://github.com/gohugoio/hugo)
* https://www.apreshill.com/blog/2017-06-up-running-with-blogdown/ -- Alison's Up and running, the go to guide
* https://bookdown.org/yihui/blogdown/ -- Yihui's book, _blogdown_
* https://emitanaka.github.io/talk/2018-08-28-rladies_melbourne_blogdown/ -- Emi's R-Ladies Melbourne Blogdown talk
* https://github.com/rstudio-education/arm-workshop-rsc2019/issues/34 -- Hosting via netlify links
* http://jmcglone.com/guides/github-pages/ -- Hosting via github
* http://jenrichmond.rbind.io/post/insights-from-the-markdown-whisperer/ -- Jenny's notes on applying Alison's custom Hugo Academic .css file.
* https://ysc-rmarkdown.netlify.com/materials/ -- Alison's _Communicating with R Markdown_ workshop, Session 4: Collections involves blogdown and styling. 
* https://app.netlify.com/drop -- Netlify _Drag & drop_ online hosting, great for trouble shooting. Drop your whole `public` folder for a temporary test.