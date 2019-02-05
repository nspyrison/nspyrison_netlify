# Blogdown: nspyrison
Standing up a blogdown site. 

### Resources:
* https://alison.rbind.io/post/up-and-running-with-blogdown/ -- Alison's Up and running, the go to that everyone points back to
* https://bookdown.org/yihui/blogdown/ -- Yihui's blogdown
* https://emitanaka.github.io/talk/2018-08-28-rladies_melbourne_blogdown/ -- Emi's R-Ladies Melbourne Blogdown talk
* https://github.com/rstudio-education/arm-workshop-rsc2019/issues/34 -- Hosting via netlify links
* http://jmcglone.com/guides/github-pages/ -- Hosting via github


### Lessons learned:
* Don't use nspyrison.github.io for agnosticism, for your first netliify go
    * May be taking Emi's hard path inadvertently (netlify and github at the same time)
* Fixxing Netlify build error 255:
    * **tldr:**
        1. Check your theme's min hugo versions [here](https://themes.gohugo.io/)
        2. In R run `blogdown::hugo_version()`
            * if you need a newer ver run `blogdown::install_hugo()`
        3. On Netlify navigate to Settings (tab along top) > Build & Deploy (menu on left) > scroll down to the Build environment variables section > Edit variables (button)
            * edit or add a Key of "HUGO_VERSION" and Value of your hugo version (*ie.* "0.53")
    * For more through documentation, see Mara's [post](https://maraaverick.rbind.io/2017/10/updating-blogdown-hugo-version-netlify/)
* Errors kniting with smalle .rda (6x2 basis):
    * can knit .rmd
    * cannot `blogdown::serve_site()` or Build, Build Website; see below error
    * workflow:
        1. `rmarkdown::clean_site()` (Build, More, Clean all)
        2. `blogdown::build_site()` , wait for build, takes a few min for me building 70 MB of manaual tours. Runs on console. (NOT build_dir(), do not run from build tab.)
        3. Push to Github (use kraken or terminal as sizes are large), hope netlify builds. Works as of SHA 6eebb990.
        * *note* no offline dev; changes are now "devele-prod"
    * Error: Error building site: "C:\Users\<some path>\dir\data\basis.rda:1:1": unmarshal of format "" is not supported
Building sites â€¦ Total in 182 ms

