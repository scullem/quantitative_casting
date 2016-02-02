# Project Objective:

This project was completed as a two week assignment for the Metis Data Science Bootcamp. My approach was to use movie data scraped from the web to find a quantitative method of making casting decisions in a film. If we assume creative and budgetary factors to be constant, can we tie a casting decision back to the potential for that cast to impact domestic total gross for a film? Imagine you are a studio casting a new comedy and have the choice between two casts: Jason Schwartzman/Rachel McAdams/Justin Long vs. Zach Galifianakis/Scarlett Johansson/Jonah Hill. Based on their histories of domestic total gross for past films, can we select the best cast based on projected contribution to domestic total gross for this new film?

# Process
* Scrape and clean movie data from Box Office Mojo & OMDb API websites
* Select scoring method for actors in a film to include as a regression feature
* Select additional features for modeling
* Use linear regression to create multiple models of Domestic Total Gross
* Select best performing model based on test & train error and adjusted R squared
* Apply findings to selecting casting for films

The code for web scraping and data cleaning can be found in the file: [02_luther_data_collection_scullem_v2.ipynb](https://github.com/scullem/quantitative_casting/blob/master/02_luther_data_collection_scullem_v2.ipynb) <br>
The code for running the models and comparing model diagnostics can be found in the file: [02_luther_dtg_ols_scullem.ipynb](https://github.com/scullem/quantitative_casting/blob/master/02_luther_dtg_ols_scullem.ipynb.ipynb) 

See the presentation below for a summary of findings:

<a href="http://www.slideshare.net/scullem/quantitative-approach-to-casting" target="_blank"><img src="images/quantitative_casting_slideshare.png" 
alt="Link to SlideShare Presentation" width="386.1" height="320.1" border="10" /></a>

<iframe src="//www.slideshare.net/slideshow/embed_code/key/i11rWtIsf2q0BD" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/scullem/quantitative-approach-to-casting" title="Quantitative approach to casting" target="_blank">Quantitative approach to casting</a> </strong> from <strong><a href="//www.slideshare.net/scullem" target="_blank">Sarah Cullem</a></strong> </div>

# Further Investigation
* Explore improvement to scoring methodology:
  * Account for the effect of inflation on Domestic Total Gross over time 
  * Weight recent film history of Domestic Total Gross more heavily
  * Account for differences in the number of Actors listed in a film
  * Identify alternative non-monetary scoring that influences the financial success of a film
* Expand to other genres in order to run model on a larger dataset (project limited to comedies from 2000-present)
* Identify supplementary data sources for films and actors
* Compare models using regularization
