# PYNAMESTATE

this is a engine to convert data from the SSI name index into a format suitable for clustering states and years on the basis of how similar names were from state to state and year to year.  Notebook assumes you're loading from an enviroment with python3, numpy, pandas, matplotlib, and scikit. 

data used here downloaded from: https://www.ssa.gov/OACT/babynames/state/namesbystate.zip

#### existing code does the following: 
- loads data from raw .csv into dataframe (converted from .txt in ssi zip)
- concatinates dataframes from each file into a larger dataframe
- imputes missing names (it'd be nice to have all names per year per state per gender to make something nice and matrix-y later on)
- calculates a score based on the fraction of births/year with a given name
- calculates similarity between states and years based on name freqency
- reduces the number of observed variables (i.e. names) via PCA
- clusters states in a given year based on similarity
- displays heatmap and scatter of clustering