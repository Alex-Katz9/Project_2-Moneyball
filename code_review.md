# Code Review: Project 2

### Name: Alex Katz

[X] README.md included

[X] Slides included

[X] Code included

## Clean Code:
**In general**
- Use comments and markdown cells a lot more frequently to make it clear what your code is doing and the intention of each step in your analysis! Your future self and any collaborators will thank you!
- Try not to leave draft code that's been entirely commented out in the final version of your notebooks/scripts. 
- Love that you saved all of your figures in your repository!
- Having all of your files in a single directory is difficult to navigate. Best practice is to create subfolders for images, noteboooks, and data files.
- Is your scraping notebook/python files missing? I may have missed them, but make sure they are included! 

**Data Cleaning notebook**
- Try and do things programmatically where possible. With pandas you can convert an entire subset of columns to numeric at once rather than calling each on in a new line, or in other cases you can use a for loop.

**EDA notebook**
- Make sure that as a final cleanup step, you re-run all your code to be sure it's working as expected, especially with notebooks since as you're working on it you may run cells out of order and end up with an analysis that isn't easily reproducible. E.g. the first cell doesn't run because you call sns.set() before importing seaborn.
- Use descriptive object names. E.g. `EA_df_subset2` => `df_numeric` or something like that. You can also include comments to indicate what this object will be used for.
- Try to avoid creating multiple copies of your dataset except when necessary. For example, no need to create a numeric-only copy of your dataframe for a heatmap. You can subset your original dataframe and plot only the subset.
- You have two versions of the `split_and_validate` funtion -- make sure to *always* use descriptive and unique object names! I suspect one of the two may have been a draft, in which case you can delete!
- I'd suggest creating a single pickle file with your features and target variables rather than a separate file for each, just to reduce clutter/the possibility of things getting out of sync.

**Modeling notebook**
- You could use sklearn's scalers for scaling features, although it's possible you had a specific reason to do it manually!
- Nice work iterating through different models and printing out the cross validation score results! A next step would be turning that code into a function you can use in the future!
- It seems like your modeling work was spread across two different notebooks (EDA and Modeling), and there were a few different approaches you took throughout, so it was a bit difficult to follow, and wasn't easy to tell what your final model ended up being. For a final product, only include your final modeling workflow, and you can note in a markdown cell what else you tried if you want to keep a record of that.

## Good Documentation:
- Good work including a detailed readme!
- Make sure to give your readme a proofread, for example there's a mention of "graduation rates" in the summary section.

## Proper Data Science:
- Good work trying a few different models and using cross validation to evaluate them.
- Nice use of RidgeCV to select optimal alpha.
- I missed where your final model evaluation on the holdout test data was. I'd make sure that's really clear in your notebooks, along with the final test data score (on whichever metric(s) you're focusing on).