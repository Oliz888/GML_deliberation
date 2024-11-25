## Unbiased Offline Recommender Evaluation for Missing-Not-At-Random Implicit Feedback  -- [reduce baised: focus on the performance indicators]
https://ylongqi.com/assets/pdf/YangCXWBE18.pdf

5.1 Experimental setup
The original dataset includes a training set and a testing set. The
training set contains 300K ratings given by 15.4K users against 1K
songs through natural interactions, and the testing set is collected
by asking a subset of 5.4K users to rate 10 randomly selected songs.
To tailor this dataset for experimenting implicit feedback, we treat
items rated greater than or equal to 4 as relevant, and others as
irrelevant, as suggested by prior literature [5]. We filter the testing
set by retaining users who have at least a relevant and an irrelevant song in the testing set and two relevant songs in the training
set (2,296 users satisfy these requirements). We additionally held
out a biased testing set (biased-testing) from the training set by
randomly sampling 300 songs for each user.
We train models discussed in Section 4.1 using the same protocol
but with fixed hyperparameters (λΘ = 0.001, training iterations:
10K, latent factors: 50). For each model, different evaluators are
used to evaluate its performance against the biased-testing set in
terms of AUC and Recall.6 The models’ true performances were
calculated by AOA over the unbiased testing set.
5.2 Results
Table 3 shows the mean absolute error (MAE) between different
evaluators’ outputs on the biased-testing set and the recommenders’
true performances. For both AUC and Recall, the unbiased evaluator (UB) reduced more than 30% of the errors in AOA, and UB’s
debiasing performance was insensitive to the hyperparameter selections. Within the range of [1.5, 3.0], UB consistently produced
significantly lower errors than AOA. However, these results also
demonstrate that UB is still imperfect, and that there is ample room
for future improvements.


## Beyond Collusion Resistance: Leveraging Social Information for Plural Funding and Voting - [Eigen Match -> Eigen voting / Page rank recommendation] 

https://download.ssrn.com/23/02/01/ssrn_id4338012_code5618274.pdf?response-content-disposition=inline&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEHEaCXVzLWVhc3QtMSJGMEQCIFDYOSWuRFFER1squlTVHVoTPfAGYpKGpa3kR7N6e%2FPqAiABzOd5tdvhH9CtBIKqJCTQHktr2S%2FPE3%2FJp%2ByXGIVVvSq9BQgZEAQaDDMwODQ3NTMwMTI1NyIMgAZo4zkI5kBU%2FzmaKpoFlbbpKC9kLiMX1hz%2F0JVnm9kKJIim9ZHD%2BKt0z1fNYvW%2F70mibevsm9axuSNbkU9nhsoe%2BhL6egheTQxVTnbGeT8KwKIYLlsG8HVdZnsZeh0ZH4B1OsUg5VaOPTRn4jaM%2BZW41PZc3A254mTLpoMVDu%2B3PYRdDcRWlB4dwhDuFrOftTBOgv0k3LNhbrR58P6KcObPBwa5rsR2zgtwHAYUTvEioFRAfGI3HOqDaGeb2w9DKO5siIzb9jMxZnOOsC%2BMzT2Rq5OSlvxmJrvcb6t3Kv8qViMPzYupusV%2BMKxedcEcchhClI1EC1ioPys%2F8ps4VLGNpoXw1QydLmrmwgCD32g5hOhAPcUVn1VePTvUthdbKqH52SNtnha7lm8ax3Fy1uTz2i3QeZQxkda3KzVHFtWUR6PafCJFje7phr%2Bhq0rgsMZ0q%2Fi3ykaGt4XUeNepbG5kbkuyt1n6K6Ugz005NfsAcVoFGLpSdRSXNIbTn7l88rL2Cnz4LIkxg9kZ3g%2B4OLU3HujOlUz8%2B4hyjDJZcAC0Xa%2F3HtwEPFnN9NT%2FENndU6KHLLUkCMVbSIDZ%2F5BKYSlXoIGr%2BGjul0Au9qKZpQX4xJ0YyRg5vVXjNCxEUS23Ia5omX0Ff55YI2zKO39HenUIN397qxm8OvLR%2BbElWe%2Fsk9%2BM%2B15OMwHbYuHyKgrMAD0%2FOKSEBzOt1YEmc8SeEICotyiaY8DR0UVIvx8FGFzCAtUvzdw%2BhJQVvzn0weC%2FZjrlbckRSnqdCa1GMlJ7QXihP010rKi%2BUWkchtBNENc9bHVguKxNJrGvn0FAiLRVzktK2cU7YFKEt9%2Bexo6FeC87V1ZCnBVX9V9GLvJ6cBat8hal2MXyqBJQFQkH178Bj%2Fmp1gBNbevFMPfAkroGOrIBodD41N4M7hC1FXXi39wgTEexCAiMt6shefWwhUsf3Ky9VlMiFbHsNCPGrM%2BUwmRYqYVRH0uVpBlJ6LCKN2xqkDg3a9MhiNFAmR75hOOasCAgt4GKB46Wbe7JmSmtA0LcgfG4vrjpfkAxX4DzT1Rfy61ZkKrixfZu5xEXZj3%2BulXG%2FN6FvzPa1HQBkvxToE2vtlkha%2FZ8NtureP4m6TPf49aymd8HLjYRYf088PqeVzoQRQ%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20241125T163025Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAUPUUPRWEXMCOYFZK%2F20241125%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=ffad8ff771679f0049cc889beb0199ff8f3e3b1c32ecbbbc27d08b86cbd804c1&abstractId=4311507
Before concluding, we will briefly present one more idea for a mechanism. This idea is relatively
undeveloped but might be one of the most promising avenues for future work.
The idea behind this mechanism, which we call EigenMatch, is to attempt to combine the
virtues of both offset and cluster match while avoiding the pitfalls of each. It is a Cluster-Matchlike procedure but under a more generalized notion of a “group”. Instead of taking in a set of
groups, this mechanism would work directly from a social graph.
The mechanism starts by calculating the eigenvectors of the adjacency matrix of the social
graph. Then, one takes the set of all eigenvectors as the set of groups and includes each agent in
each group with a weight corresponding to that agent’s index of that group’s eigenvector. Then,
one utilizes these weights to calculate “group contribution” and does normal QF on the group
contributions, as in Cluster Match.
Formally, let E be the set of eigenvectors of a social graph. Then EigenMatch might calculate
the funding amount as


