# Model-Evaluation
Implementing Random Selection and Upper Confidence Bound

This code is implementing two different algorithms for solving the Multi-Armed Bandit problem using simulations and visualizing the results. The Multi-Armed Bandit problem is a classic problem in probability theory and decision-making where you have a set of options (arms), each with an unknown probability distribution of providing rewards. The goal is to find the arm that maximizes the total reward over a series of trials.

Here's a breakdown of what the code does in English:

Random Selection:

Import necessary libraries such as NumPy, Matplotlib, and Pandas.
Read a dataset named 'Ads_CTR_Optimisation.csv' using Pandas.
Initialize parameters N (number of rounds) and d (number of arms or ads).
Create empty lists 'ads_selected' to store the selected ads and 'total_reward' to track the cumulative reward.
Loop through N rounds:
Select a random ad (arm) from the available options (0 to d-1).
Record the selected ad.
Retrieve the reward associated with the selected ad from the dataset.
Update the total_reward by adding the reward.
After the simulation, it visualizes the results by plotting a histogram showing how many times each ad was selected.

Upper Confidence Bound (UCB) Selection:

Import necessary libraries.
Reinitialize parameters N and d.
Create additional lists 'numbers_of_selections' to count the number of times each ad was selected and 'sums_of_rewards' to track the cumulative rewards for each ad.
Loop through N rounds:
For each round, calculate the UCB for each ad and select the ad with the highest UCB.
The UCB for each ad combines the average reward and an exploration term based on the number of times the ad has been selected.
Update the statistics for the selected ad (count and reward).
Update the total_reward.
Like the random selection, it visualizes the results by plotting a histogram of ad selections.

In summary, the code first performs a random selection strategy where ads are chosen randomly in each round, and then it implements the UCB algorithm, which makes more informed decisions based on estimated ad performance. The histograms at the end show how many times each ad was selected in both cases, allowing you to compare the performance of the two strategies in terms of total reward.
