# Global Shark Attack Incidents

## Ironhack's Data Analytics Bootcamp Project I: Data Cleaning and Manipulation with Pandas

![Don't think sharks are adorable?](/images/shark.jpeg)

## 

I started with this messy data set: [Shark Attack](https://www.kaggle.com/teajay/global-shark-attacks/version/1). I imported it, used my data wrangling skills to clean it up, prepared it to be analyzed, and then exported it as a clean CSV data file.

### Main goal and hypotheses:

As a biologist, my goal with this project was to demonstrate that sharks are adorable creatures and that humans seek to be eaten by them for some strange reasons.

**My hypotheses:**

* Most attacks are not **fatal** because, you know, sharks are cute.
* Humans get into the sea in any **month** of the year.
* With each passing **year** (and **century**), more people go swimming in the sea.
* Humans do some weird stuff (**activities**) to make it easier for sharks to locate them.
* Are you a woman (female **sex**)? [Good news: you're probably not going to get bitten by a shark](https://www.smh.com.au/environment/conservation/fact-sharks-pretty-much-only-bite-men-heres-why-20151029-gklnxo.html).
* Most attacks are of **type** provoked. If plots say otherwise, they lie.
* [It is ok to feed sharks with tender meat](https://www.elmundotoday.com/2010/04/un-colegio-de-miami-lleva-a-sus-alumnos-conflictivos-a-ver-de-cerca-a-los-tiburones/) (young **age** people).
* USA will be the most affected **country**, [because it is the cradle of jazz](https://www.theguardian.com/music/2018/may/10/sharks-love-jazz-macquarie-university-sydney).

### Methods:

I first imported the packages I needed. Then, I imported the dataframe using Pandas with the correct encoding.

Afterwards, I took a first look at the data. The initial messy data set had 24 columns and 5992 rows. I decided to work with the following variables:
1. Fatal (Y/N)
1. Month
1. Year
1. Century
1. Activities
1. Sex
1. Type
1. Country

I cleaned them up and performed some graphical representations.

For more information about methods, see the file *data-wrangling.ipynb*.

### Results:

* Most attacks are not fatal (73.6% vs. 26.4%). ✔️
* Humans get into the sea in any month of the year. ✔️
* There are more registered attacks now than in the past. ✔️
* Sharks mostly bite victims who are swimming, surfing, fishing or diving. ✔️
* Sharks mostly attack men (89.2% male vs. 10.8% female). ✔️
* Most attacks are unprovoked (89.8% unprovoked vs. 10.2% provoked). ❌
* Sharks mostly attack young people (maximum at about 20 years old). ✔️

### Deliverables:

* The initial messy data set can be found in the *Input* folder.
* The Jupyter Notebook *data-wrangling.ipynb* contains all Python code and commands used in the importing, cleaning, manipulation, and exporting of the data set.
* The cleaned CSV data file containing the results of my data wrangling work can be found in the *Output* folder.
* The *src* folder contains the file *functions.py*, which stores some own functions I have imported and used at *data-wrangling.ipynb*.

### Obstacles encountered and lessons learned:

The biggest obstacle I encountered was to deal with missing values. I learned that when introducing NAs into an existing Series or DataFrame via reindex() or some other means, boolean and integer types are promoted to a different dtype in order to store the NAs. More information about this topic can be found [here](https://pandas.pydata.org/pandas-docs/stable/user_guide/gotchas.html).

I also had to invest some time in cleaning up the 'Activity' variable in order to get as much information from it as possible.