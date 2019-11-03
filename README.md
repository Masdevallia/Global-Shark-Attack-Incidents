# Global Shark Attack Incidents

## Ironhack's Data Analytics Bootcamp Project I: Data Cleaning and Manipulation with Pandas

![Don't think sharks are adorable?](/images/shark.jpeg)

## 

I have started with this messy data set: [Shark Attack](https://www.kaggle.com/teajay/global-shark-attacks/version/1). I have imported it, used my data wrangling skills to clean it up, prepared it to be analyzed, and then exported it as a clean CSV data file.

### Deliverables:

* The initial messy data set can be found in the *Input* folder.
* The Jupyter Notebook *data-wrangling.ipynb* contains all Python code and commands used in the importing, cleaning, manipulation, and exporting of the data set.
* The cleaned CSV data file containing the results of my data wrangling work can be found in the *Output* folder.
* The *src* folder contains the file *functions.py*, which stores some own functions I have imported and used at *data-wrangling.ipynb*.

### Obstacles encountered and lessons learned:

The biggest obstacle I encountered was to deal with missing values. I learned that when introducing NAs into an existing Series or DataFrame via reindex() or some other means, boolean and integer types are promoted to a different dtype in order to store the NAs. More information about this topic can be found [here.](https://pandas.pydata.org/pandas-docs/stable/user_guide/gotchas.html)

I also had to invest some time in cleaning up the 'Activity' variable in order to get as much information from it as possible.