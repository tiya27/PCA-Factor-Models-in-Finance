Part 1 was about data preparation, Part 2 - extracts hiddent market structure.
PCA tries to answer - Can we summarize movements of 10 stocks using only a few hidden factors, where instead of 10 independent dimensions, 2-3 components explain most behaviour - dimensionality reduction.

2(a) - 
- perform PCA - builds covariance matrix and decompose it into eigenvectors and eigenvalues.
- extract eigenvalues eigenvectors
- scree plot - shows importance of each principal component - most information concentrated in first few PCs
- explained variance
- determine components req for >= 80% variance.

Perform PCA
- PCA Analyzes covariance structure of standardized returns and finds -
    - principal directions
    - explained variance
    - latent factors

eigenvectors - directions of movement - hidden factors

eigenvalues - how important each above factor is

If scree plot graphs frop quickly - market behavior is dominated by few hidden factors

2(b) - 
compares PCA on standardized returns vs PCA on unstandardized returns.

- we have raw log returns without standardization
- we are observing PCA on this to observe how volatality biases PCA

Eigenvalue comparision - 
- standardized pca - all stocks on same variance scale - so eigenvalues reflect shared variance/correlation
- raw pca - larger volatility stocks produce larger covariance value - larger eiegnevalues

PCA scores - projection of data onto the principal directions. scores tell how strongly each day behaves according to that PC.
scores behaves like market activity indicators.

Loading tells how each stock contributes to a PC, describes the variables and features

