# ACM Research Coding Challenge (Fall 2020)

## No Collaboration Policy

**You may not collaborate with anyone on this challenge.** You _are_ allowed to use Internet documentation. If you _do_ use existing code (either from Github, Stack Overflow, or other sources), **please cite your sources in the README**.

## Submission Procedure

Please follow the below instructions on how to submit your answers.

1. Create a **public** fork of this repo and name it `ACM-Research-Coding-Challenge`. To fork this repo, click the button on the top right and click the "Fork" button.
2. Clone the fork of the repo to your computer using . `git clone [the URL of your clone]`. You may need to install Git for this (Google it).
3. Complete the Challenge based on the instructions below.
4. Email the link of your repo to research@acmutd.co with the same email you used to submit your application. Be sure to include your name in the email.

## Question One

![Image of Cluster Plot](ClusterPlot.png)
<br/>
Given the following dataset in `ClusterPlot.csv`, determine the number of clusters by using any clustering algorithm. **You're allowed to use any Python library you want to implement this**, just document which ones you used in this README file. Try to complete this as soon as possible.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file.

Answer:
First, I would locate the apparent clusters on the graph. Then, I would pick 1-2 coordinate points from the most and 1-2 from 
the least dense parts of those clusters, depending on how spread apart the points are, and store each in a variable called "reference." 
I would then set a range of x and y values to compare the closeness. In the case of this specific graph, I would use the x-value +/- 1 
in each direction and y-value +/- 1 in each direction. For example, I would see how many points fit the values of (4 + 1, 0.9 + 1) 
and (4 - 1, 0.9 - 1). If the coordinate points of surrounding points fall within this range, I would count them and store them in a 
distinct variable or assign them a specific color. If not, I would compare it to the next reference point with the same range until 
the coordinate points run out. If the coordinate point has already been counted, it would be ignored. By the end of this, I should 
have smaller clusters and a few outlying points that didn't fit in that range. I would then allocate any remaining points to the 
nearest reference points.