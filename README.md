Game of Life
===
Benjamin J. Radford  
[My website](http://www.benradford.com)

Implementation of [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway's_Game_of_Life) in [R Shiny](http://shiny.rstudio.com/). The app can be run locally from within [R](http://www.r-project.org/) using the [Shiny](http://cran.r-project.org/web/packages/shiny/index.html) package. Alternatively, the app is hoted online at [https://benradford.shinyapps.io/game_of_life/](https://benradford.shinyapps.io/game_of_life/).

Parameters
---

*Step*  
Cycles through or animates the first 250 iterations of the game. These states are pre-calculated but the images are generated on-the-fly.

*Starting Proportion*  
The app populates a 40 by 40 cell grid with randomly selected "live" cells. The proportion of starting cells can be given via a slider input. 

*Born if next to*  
Cells are "born" if they are bordered by the number of surrounding cells specified in the text field "Born if next to." This can be specified as a list of integer values 1-8. The default value is 3 as in Conway's original version, but alternates can be provided. For example, a value of "36" would specify that new cells are born if they are surrounded by either 3 or 6 living cells.

*Stays if next to*  
Living cells continue to live into the next iteration if they are surrounded by either 2 or 3 living cells. These values can be changed by altering the "Stays if next to" parameter. Lists of integer values are accepted.

*Gosper Glider Gun*  
A [Gosper glider gun](http://www.conwaylife.com/wiki/Gosper_glider_gun) can be created by entering either "glider" or "gun" into either of the available text fields and pressing "Refresh".  Because the grid wraps around the edges, the gun will shoot itself after several iterations.