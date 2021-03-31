### mod19
## Overview of Analysis:
Our goal was to predict the success or failure of applicants for Alphabet Soup, and more specifically to train and optimize a neural network to determine its efficacy on this problem.

## Results:
The target was a binary "success" or "failure" column, and our features included monetary values, codes and categories, application type, as well as ID columns. We dropped the unimportant ID and Name columns from the features set. The data started with several categorical variables, each of which had far too many values for 1 hot encoding to be effective. We analyzed the "value_counts" for each column and determined cutoff points, below which all categores were simply listed as "other". We scaled the X data after that; admittedly more analysis on the actual data should be done before moving to another model.

To compile and train the model we begain with a straight relu model with 2 hidden layers with 6 nodes each. That model was trained for 100 epochs and weights were saved every 5th epoch. The final accuracy (on the test set) was just under 73%. We added layers and attempted to modify both number of nodes and activation functions for each node, but without diving further into the data our best attempt topped out at 73.03% - better, but still a far cry from the target of 75%. 

## Summary
These results are promising, but significantly more time is needed on pre-processing to fully explore the potential of nn. Exploring a log_reg and/or SVM algo would be worthwhile as these algorithms may provide similar accuracy for much less work, and they both are well suited to linear classification problems.
