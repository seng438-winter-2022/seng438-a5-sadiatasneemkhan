**SENG 438- Software Testing, Reliability, and Quality**

**Lab. Report \#5 – Software Reliability Assessment**
| Group \:  35     |            |
|-------------------|------------|
| Student Names:    |    UCID    |
| Luis Sulbaran     | 30090906   |
| Adam Abouelhassan | 30087777   |
| Jaxson Waterstreet| 30095706   |  
| Sadia Khan        | 30090271   |

# Introduction
The objective of this lab was to analyze integration test data using reliability assessment tools. The two methods that were implemented in order to assess the failure data were reliability growth testing and reliability demonstration charts (RDC) for the reliability assessment. Covariate Software Failure and Reliability Assessment Tool, know as C-SFRAT, was our selected reliabitlity growth tool.

# Assessment Using Reliability Growth Testing 

## Result of model comparison (selecting top two models)
Using the C-SFRAT tool, we were able to plot all the models and covariates and analyze the trend between the plotted data. The models selected include:

- IFR Salvia and Bollinger
- S Distribution
- Discrete Weibull (Order 2)
- IFR Generalized Salvia and Bollinger
- Negative Binomial (Order 2)
- Geometric
- Truncated Logistic

When finding the best two models, C-SFRAT made it easy to compare the different models using the model comparison tab which allowed us to see which one would fit the best into our failure data. We used the Log-Likelihood to determine which fit best as it is used as a way to measure the goodness of fit for a model.

As shown in the image below, the top two models for our failure data are DW3 on F, and IFRGSB on E, F.
![p1](https://user-images.githubusercontent.com/81999006/162554587-f562ee63-2969-491f-a6cf-8d4a83b8df1a.png)

## Result of range analysis (an explanation of which part of data is good for proceeding with the analysis)	

To determine the range analysis that was good enough for proceeding, we looked at the failure data and the failure count per time interval.  Since any general failure data must contain at least 50 failures for proper analysis, we were able to analyze the data more accurately from about interval 14 and further. We also looked at the data that would fit the points on the failure data graph best which gave about the same result as above.

## Plots for failure rate and reliability of the SUT for the test data provided	

### MVF Graph
![mvf](https://user-images.githubusercontent.com/81999006/162554692-6c7e9c5b-44a2-44e3-ae17-9b82fdae1cde.png)

### Intensity Graph
![intensity](https://user-images.githubusercontent.com/81999006/162554690-fe060d14-b163-48b4-a219-1600c4e75b91.png)

### Reliability Graph Prediction
![reliability graph prediction](https://user-images.githubusercontent.com/81999006/162554693-8af29c6d-04c9-4afe-99c9-fba8d96f0e6a.png)

## A discussion on decision making given a target failure rate	

For the target failure rate, we used the C-SFRAT tool to observe the results of each interval we tested until we finally arrived at the target failure shown in the image above. We wanted to ensure the target was low enough to ensure data reliability. However, we also wanted to gather accurate data from both models using the intensity graph as a measure of what was acceptable (~0.4). This target made the system reasonable to accept as the higher numbers we tested, the intensity range became way too large for the prediction we came up with.

## A discussion on the advantages and disadvantages of reliability growth analysis

An advantage of reliability growth analysis is you have options to either inter failure times or failure count against MTTF. Reliability growth analysis allows the tracking of bugs in pre-release, provides a guide to the software testing process and gives an idea of when the product is ready to be released. Some disadvantages of reliability growth analysis are that for an accurate analysis you need the proper tools and a good amount of failure data to get proper measurements. Also if an incorrect model is selected the results might not be optimal.

# Assessment Using Reliability Demonstration Chart 

## 3 plots for MTTFmin, twice and half of it for your test data	
## Explain your evaluation and justification of how you decide the MTTFmin	
## A discussion on the advantages and disadvantages of RDC

Some of the main advantages of using RDC is that it gives us a clear visual representation of what the failure rate of the SUT is. This is very important when testing a system as it gives us an idea on whether the system is reliable enough to deploy. One disadvantage of RDC is that even though it displays the number of failures per unit time, it does not tell us how/why the system failed, which is important for debugging the system. 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

Both of these two techniques are based on inter failure times and target failure rate (or MTTF). But RDC is based solely on inter failure time and MTTF while reliability growth analysis can use failure times and/or failure count with MTTF. During this lab we became familiar with some reliability testing tools and learned the importance of seeking assistance from peers and resources when confused by a new tool as we ran into some issues using these tools in this lab.

# How the team work/effort was divided and managed


# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
