This repository contains two folders:
1. IMDb Dataset,
2. Experiment Results.

### 1. IMDb Dataset Folder
The folder contains the Internet Movie Database (IMDb) dataset and problem instances used in experiments over the team forming hybrid genetic algorithm for team formation problem considering social network. This dataset contains information about the actors with the list of movies in which they have performed between the years 2000 and 2002. There are 1021 actors with 27 distinct skills which are the genres of the movies.
#### Content:
- rpsd.txt contains the real person-skill data which is a person x skill matrix having 1 if the person has the corresponding skill, 0 otherwise.

- mpsd.txt contains the modified person-skill data which is a person x skill matrix having 1 if the person has the corresponding skill, 0 otherwise. This matrix is used by Berktaş (2021) in her PhD. thesis.
- network_distances.txt contains the distances/communication cost in the social network which is a person x person matrix.
	- For a collaborated pair, communication cost is calculated according to Jaccard’s distance metric so that these weights are between zero and one.
	- For an uncollaborated pair, the communication cost is equal to the minimum distance between them in social network graph.
	- For an unconnected pair, the communication cost is set to a sufficiently large number.
	- Diagonal values are zero.

- instances.txt contains 900 team formation problem instances, namely tasks, we use and Berktaş used.
	- ID is the instance ID.
	- |T| is the number of required skills, element of {4,6,8,10,12,14,16,18,20}.
	- T is the list of required skills to accomplish the task.
	- |V'| is the number of qualified people for the task, i.e. the number of people having at least one of the required skills.

### 2. Experiment Results Folder
The folder contains the results obtained in the experiments the team forming hybrid genetic algorithm.
#### Content:
- Results (RPSD).xls contains obtained objective values, elapsed times and iteration counts by using the real person skill data.
	- All Results (RPSD) sheet contains the records obtained in each run (900 instances * 10 runs = 9000 results).
	- Summarized Results (RPSD) sheet contains the results calculated by finding average/minimum/maximum of the records in each run (900 results).

- Results (MPSD).xls contains obtained objective values, elapsed times and iteration counts by using the modified person skill data.
	- All Results (MPSD) sheet contains the records obtained in each run (900 instances * 10 runs = 9000 results).
	- Summarized Results (MPSD) sheet contains the results calculated by finding average/minimum/maximum of the records in each run (900 results).
	- Times Considering CPU Ranks sheet contains the times calculated by considering the CPU ranks of Intel Core i7-6700HQ and Intel Core2 Quad Q9400 given by Geekbench,UserBenchmark and PassMark.

*Berktaş, N. (2021). Deterministic and Stochastic Team Formation Problems [Bilkent University]. http://repository.bilkent.edu.tr/handle/11693/75539*
