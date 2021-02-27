# Setup instructions

```bash
conda conda env create -f "environment.yml"
conda activate sc-notebook
PYTHONHASHSEED=0 jupyter notebook
```

# List of Notebooks
* `CalLink Scraping Analysis` - This notebook has the code for scraping the CalLink emails and other info into a nicely packed JSON file. Also includes charts for showing some statistics based on collected variables.
* `Future Sign Up Analysis` - This notebook was used to compare and contrast between the data scraped from CalLink and the data from the beta waitlist back in the summer of 2020.
* `UC Berkeley Majors & Minors Scraping` - This notebook is used for scraping all the majors and minors as part of the student account registeration. This is yet to be used until the student accounts project is back online.
* `Generic Club Recommendations` - This notebook contains the logic for the club recommendations. Includes many charts and visual graphs for debugging and post-analysis based on distributions and network analysis.


# Note about reproducibility with ML models
 You need to set the `PYTHONHASHSEED` to `0` to fix the seed used for hash randomization. It's needed along with setting the random seed for the Word2Vec model to `42` and using only 1 worker to create the exact same model with the same exact data 100% of the time.

* Source: https://stackoverflow.com/a/30586046
