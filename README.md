# Preventative-Maintenance-using-AI-ML-ModelsProject: Preventative Maintenance Using AI/ML models
Dataset: Predictive Maintenance Dataset

# Business Problem
Predictive Maintenance (PdM) in the industrial context refers to the use of data, analytics, and 
machine learning techniques to predict when equipment or machinery is likely to fail. By 
analyzing the condition and performance of equipment in real-time, organizations can take 
proactive measures to perform maintenance just in time, maximizing asset uptime, and 
minimizing downtime and associated costs.
Predictive Maintenance is widely adopted in industries with critical and expensive machinery, 
such as manufacturing, energy, transportation, and healthcare. The goal is to transition from a 
reactive or preventive maintenance approach to a more proactive and data-driven strategy, 
ultimately improving reliability, efficiency, and overall operational performance.
In this study Predictive Maintenance Dataset (AI4I 2020) from Kaggle is selected to perform 
predictive Maintenance Analysis on this. This synthetic dataset is modeled after an existing 
milling machine and consists of 10 000 data points from a stored as rows with 14 features.

# Dataset description:
The dataset consists of 14 columns and 10000 records described below:
1- UID: unique identifier ranging from 1 to 10000.
2- 2- Product ID: consisting of a letters
• L: low (50% of all products)
• M: medium (30%)
• H: high (20%)
• As product quality variants and a variant-specific serial number.
3- Type: just the product type L, M or H from column 2.
4- Air temperature [K]: generated using a random walk process later normalized to a 
standard deviation of 2 K around 300 K.
5- Process temperature [K]: generated using a random walk process normalized to a standard 
deviation of 1 K, added to the air temperature plus 10 K.
6- Rotational speed [rpm]: calculated from a power of 2860 W, overlaid with a normally 
distributed noise.
7- Torque [Nm]: torque values are normally distributed around 40 Nm with a SD = 10 Nm 
and no negative values.
8- Tool wear [min]: The quality variants H/M/L add 5/3/2 minutes of tool wear to the used 
tool in the process.
9- A 'machine failure' label that indicates whether the machine has failed in this datapoint 
for any of the following failure modes are true.
10- The machine failure consists of five independent failure modes.
11- Tool Wear Failure (TWF): the tool will be replaced of fail at a randomly selected tool 
wear time between 200 - 240 mins (120 times in our dataset). At this point in time, the 
tool is replaced 69 times, and fails 51 times (randomly assigned).
12- Heat Dissipation Failure (HDF): heat dissipation causes a process failure, if the difference 
between air- and process temperature is below 8.6 K and the tools rotational speed is 
below 1380 rpm. This is the case for 115 data points.
13- below 3500 W or above 9000 W, the process fails, which is the case 95 times in our 
dataset.
14- Overstrain Failure (OSF): if the product of tool wear and torque exceeds 11,000 minNm 
for the L product variant (12,000 M, 13,000 H), the process fails due to overstrain. This 
is true for 98 datapoints.
15- Random Failures (RNF): each process has a chance of 0,1 % to fail regardless of its 
process parameters. This is the case for only 5 datapoints, less than could be expected for 
10,000 datapoints in our dataset.
If at least one of the above failure modes is true, the process fails, and the 'machine failure' label 
is set to 1. It is therefore not transparent to the machine learning method, which of the failure 
modes has caused the process to fail.

# Objective:
This study intended to offer a practicable model capable of predicting possible failure in machine, 
to help industries minimize failure risks in their machines.
