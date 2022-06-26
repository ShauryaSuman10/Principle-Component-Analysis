# Principle-Component-Analysis

Somewhat unsurprisingly, reducing the dimension of the feature space is called “dimensionality reduction.” There are many ways to achieve dimensionality reduction, but most of these techniques fall into one of two classes:  
1. Feature Elimination 
2. Feature Extraction 

Feature elimination is what it sounds like: we reduce the feature space by eliminating features. In the example above, instead of considering every single variable, we might drop all variables except the once we think will best predict the cancer. Advantages of feature elimination methods include simplicity and maintaining interpretability of your variables.  As a disadvantage, though, you gain no information from those variables you’ve dropped. By eliminating features, we’ve also entirely eliminated any benefits those dropped variables would bring.  

Feature extraction, however, doesn’t run into this problem. Say we have ten independent variables. In feature extraction, we create ten “new” independent variables, where each “new” independent variable is a combination of each of the ten “old” independent variables. However, we create these new independent variables in a specific way and order these new variables by how well they predict our dependent variable.  

You might say, “Where does the dimensionality reduction come into play?” Well, we keep as many of the new independent variables as we want, but we drop the “least important ones.” Because we ordered the new variables by how well they predict our dependent variable, we know which variable is the most important and least important. But — and here’s the kicker — because these new independent variables are combinations of our old ones, we’re still keeping the most valuable parts of our old variables, even when we drop one or more of these “new” variables!  

Principal component analysis is a technique for feature extraction — so it combines our input variables in a specific way, then we can drop the “least important” variables while still retaining the most valuable parts of all of the variables! As an added benefit, each of the “new” variables after PCA are all independent of one another. This is a benefit because the assumptions of a linear model require our independent variables to be independent of one another. If we decide to fit a logistic regression model with these “new” variables (see “principal component regression” below), this assumption will necessarily be satisfied.
