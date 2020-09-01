# TrojAI-r2-filter-falsepositives

This repo contains folders `benigns` and `trojans`. Folder `benign` contains benign images of 1 label which can be consistantly misclassied to another label when stamped with a filter.
Folder `trojan` contains images of `benigns` folder stamped with the filter.
For example, in folder `benigns/id-00000102` contains the original images and folder `trojans/id-00000102` contains the images in `benigns/id-00000102` stamped with a filter.

This repo also contains folder `ground_truth_filters` where I list the ground truth images of model id-00000078 and model id-00000082 to help illusrate that the filters presented in 
`trojans` visually does not create a larger perturbation compared to ground truth filters.

You can check the file `calc_ssim.py` to check the ssim score between filtered images and benign images. The following table shows the ssim score between images of each model.
We can see the ssim score the images false positive models are mostly over 0.8 (46 out of 50) and at least 0.7 while ssim score for the 2 set of ground truths images are 0.5 and 0.7 respectively.

| Images to calculate SSIM           | Images to calculate SSIM | SSIM       |
|------------------------------------|--------------------------|------------|
| ./trojans/id-00000063              | ./benigns/id-00000063    | 0.8650817  |
| ./trojans/id-00000090              | ./benigns/id-00000090    | 0.8214894  |
| ./trojans/id-00000102              | ./benigns/id-00000102    | 0.87533575 |
| ./trojans/id-00000123              | ./benigns/id-00000123    | 0.85307807 |
| ./trojans/id-00000129              | ./benigns/id-00000129    | 0.9456398  |
| ./trojans/id-00000141              | ./benigns/id-00000141    | 0.9356979  |
| ./trojans/id-00000153              | ./benigns/id-00000153    | 0.8494666  |
| ./trojans/id-00000174              | ./benigns/id-00000174    | 0.9567677  |
| ./trojans/id-00000180              | ./benigns/id-00000180    | 0.9752297  |
| ./trojans/id-00000190              | ./benigns/id-00000190    | 0.8628585  |
| ./trojans/id-00000192              | ./benigns/id-00000192    | 0.9225216  |
| ./trojans/id-00000208              | ./benigns/id-00000208    | 0.8402901  |
| ./trojans/id-00000231              | ./benigns/id-00000231    | 0.7730729  |
| ./trojans/id-00000232              | ./benigns/id-00000232    | 0.8843335  |
| ./trojans/id-00000235              | ./benigns/id-00000235    | 0.889655   |
| ./trojans/id-00000241              | ./benigns/id-00000241    | 0.9058631  |
| ./trojans/id-00000242              | ./benigns/id-00000242    | 0.8865626  |
| ./trojans/id-00000249              | ./benigns/id-00000249    | 0.930513   |
| ./trojans/id-00000266              | ./benigns/id-00000266    | 0.8366065  |
| ./trojans/id-00000284              | ./benigns/id-00000284    | 0.9090895  |
| ./trojans/id-00000288              | ./benigns/id-00000288    | 0.9725411  |
| ./trojans/id-00000295              | ./benigns/id-00000295    | 0.8767611  |
| ./trojans/id-00000301              | ./benigns/id-00000301    | 0.7002666  |
| ./trojans/id-00000321              | ./benigns/id-00000321    | 0.9182148  |
| ./trojans/id-00000326              | ./benigns/id-00000326    | 0.88213766 |
| ./trojans/id-00000331              | ./benigns/id-00000331    | 0.99419683 |
| ./trojans/id-00000347              | ./benigns/id-00000347    | 0.9129259  |
| ./trojans/id-00000357              | ./benigns/id-00000357    | 0.8860453  |
| ./trojans/id-00000365              | ./benigns/id-00000365    | 0.88479483 |
| ./trojans/id-00000370              | ./benigns/id-00000370    | 0.8372718  |
| ./trojans/id-00000381              | ./benigns/id-00000381    | 0.8198655  |
| ./trojans/id-00000388              | ./benigns/id-00000388    | 0.85057634 |
| ./trojans/id-00000391              | ./benigns/id-00000391    | 0.92746776 |
| ./trojans/id-00000402              | ./benigns/id-00000402    | 0.9648509  |
| ./trojans/id-00000405              | ./benigns/id-00000405    | 0.9127963  |
| ./trojans/id-00000411              | ./benigns/id-00000411    | 0.92258286 |
| ./trojans/id-00000415              | ./benigns/id-00000415    | 0.8851233  |
| ./trojans/id-00000416              | ./benigns/id-00000416    | 0.87887055 |
| ./trojans/id-00000429              | ./benigns/id-00000429    | 0.8582368  |
| ./trojans/id-00000437              | ./benigns/id-00000437    | 0.95905185 |
| ./trojans/id-00000447              | ./benigns/id-00000447    | 0.89220005 |
| ./trojans/id-00000449              | ./benigns/id-00000449    | 0.92651343 |
| ./trojans/id-00000457              | ./benigns/id-00000457    | 0.81368583 |
| ./trojans/id-00000459              | ./benigns/id-00000459    | 0.84097046 |
| ./trojans/id-00000469              | ./benigns/id-00000469    | 0.93074787 |
| ./trojans/id-00000471              | ./benigns/id-00000471    | 0.9053568  |
| ./trojans/id-00000478              | ./benigns/id-00000478    | 0.8754884  |
| ./trojans/id-00000497              | ./benigns/id-00000497    | 0.9189833  |
| ./trojans/id-00000498              | ./benigns/id-00000498    | 0.90751827 |
| Ground Truths filter Images        |                          |            |
| ./ground_truth_filters/id-00000078 | ./benigns/id-00000078    | 0.5229215  |
| ./ground_truth_filters/id-00000082 | ./benigns/id-00000082    | 0.7014901  |
