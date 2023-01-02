# Data and methods
Psychopathy is an antisocial personality disorder that is highly correlated with crime and violence. Psychopathy Check List Revised (PCL-R) provides a clinical assessment of the degree of psychopathy that an individual possesses. Specific scoring criteria rate twenty separate items on a three-point scale (0, 1, 2) to determine the extent to which they apply to a given individual. In this analysis we do Partial-Least-Squares (PLS) analysis on sMRI images of PCL-R assessed forensic patients, to see if there exists reliable biomarkers that correlate with the subscores of the PCL-R. Sample size is 51. As preprocessing, grey matter (GM) images are segmented from the sMRI images with SPM software. Then, regional volumes are calculated from the GM images with masks provided also by the SPM software. These regional volumes are then normalized with total GM volume, so that we analyze volumes relative to individuals total GM volume instead of analyzing absolute volumes.

PLS aims to find latent components (linear combinations) from both, volume features X and behavior measures Y, that maximally correlate. This is achieved by doing Singular-Value-Decomposition (SVD) on the correlation matrix R which is calculated from normalized X (X0) and normalized Y (Y0) as R = transpose(Y0) * X0.

# Results

![image](https://user-images.githubusercontent.com/40278371/210245355-de3a4b25-99de-496a-a1f0-506dafdb5b91.png)

In the plot, warm areas (red) are positively correlated with behavior scores, which is to say that the GM volume tends to increase with the behavior scores in these areas. Cold areas (blue) are negatively
correlated, which is to say that GM volume tends to decrease in these areas with increase in behavior scores.

![image](https://user-images.githubusercontent.com/40278371/210245429-e2f43467-7488-48be-9bb8-e66e4a296ee6.png)

![image](https://user-images.githubusercontent.com/40278371/210245622-dda89ccf-e155-4b7f-8637-ff2fe72dc6f5.png)

# Conclusions

There seems to be a moderate negative correlation between the relative volumes of the following brain regions and the following behavior scoring:

Brain regions, correlation direction:
- Left MSFG superior frontal gyrus medial segment, -
- Right OrIFG orbital part of the inferior frontal gyrus, -
- Left PoG postcentral gyrus, -
- Left FRP frontal pole, +

Behaviors:
- Need for Stimulation/Proneness to Boredom
- Poor Behavioral Controls
- Irresponsibility

The findings however are cofounded by the used scanner (especially by the use of Siemens scanner). This means we can't conclude if the differences are due to the antisocial behavior or due to
different scanners being used.
