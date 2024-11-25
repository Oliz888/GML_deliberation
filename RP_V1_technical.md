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

## Does Enclave Deliberation Polarize Opinions?

When like-minded people discuss with each other, i.e. engage in ‘enclave deliberation’, their opinions tend to become more extreme. This is called group polarization. A population-based experiment with a pre-test post-test design was conducted to analyze whether the norms and procedures of deliberation interfere with the mechanisms of group polarization. Based on a survey, people with either permissive or restrictive attitudes toward immigration were first identified and then invited to the experiment. The participants were randomly assigned to like-minded and mixed small-n groups. Each like-minded group consisted of only permissive or restrictive participants, whereas each mixed group consisted of four permissive and four restrictive participants. The like-minded treatment represents enclave deliberation, and the mixed treatment a ‘standard’ deliberative mini-public design. The main finding of our experiment is that people with anti-immigrant attitudes become more tolerant even when they deliberate in like-minded groups. Moreover, similar learning curves are observed in both treatments. Based on the results, we conclude that deliberative norms can alleviate the negative consequences of discussion in like-minded groups.

https://link.springer.com/article/10.1007/s11109-015-9304-x#Sec3

H1a Deliberation in like-minded groups leads to a polarization of opinions.

H1b Deliberation in mixed groups de-polarizes opinions.

H2a Deliberation in like-minded groups amplifies cognitive errors.

H2b Deliberation in mixed groups corrects cognitive errors.


## Could selective use of AI lighten the load? - [case using AI/self-organizing structure in the deliberation]
https://www.niemanlab.org/2024/07/could-social-media-support-healthy-online-conversations-new_public-is-working-on-it/
Since moderating these groups can be such a time suck, Doshi and Pariser are thinking about ways to harness a tool that might not sound like it belongs in a conversation about civic connection and healthy online discourse: generative AI. (They’re not alone — Facebook is piloting AI tools for its group admins, too.)

“AI can play a really important role in reducing this care labor that these stewards are putting in,” Doshi said. The thinking is that AI tools can take on more mundane, time-consuming tasks like (in most cases) verifying whether a prospective member of a given group is actually a member of a given community. It can help take over work where there isn’t a difficult, human judgment call needed — including by acting as a kind of filter to sort out comments that are clearly in-line or out-of-line, and flagging the ones that are edge cases for human moderation.

Doshi pointed to one example of successful self-moderation in a Facebook group with nearly 2 million members. The group, established by Lola Omolola in 2015, was originally called Female in Nigeria (FIN) (now, to reflect its more international focus on women’s issues, it’s called Female IN). The group’s moderators invented a “grumpy cat,” Doshi said, to help gently set and sustain the tone and culture of the group. If someone posts something at risk of breaking the group’s guidelines, users can post the grumpy cat as a shared tool for keeping the conversation civil.

“The grumpy cat is a tool that the moderators use to say ‘this is not exactly what this group is for,’” Doshi explained. “I think that this is an example of where AI can be trained on this kind of spectrum of norms, and then take that work off of the individuals to have to do it.”


## How we're building with international public broadcasters - [value study: Creating and measuring dynamic public value - metrics design]  
https://newpublic.substack.com/p/how-were-building-with-international
Design for public value, not just individual value
We believe that this project’s approach to design and product for public broadcasters has the potential to elevate public conversation to the same level of importance as the broadcasters’ world-class journalism. This might seem like a tall ask: directing audience members’ finite attention to participating in discussion could mean diverting their time and attention away from business-driven objectives like advertising (revenue) or account sign-ups (retention). But the public broadcasters’ mission to strengthen public conversation gives us the space to fully invest in these explorations.

Ultimately, investing in these principles means conceiving of “value” on the internet differently. Product development in the tech industry has traditionally aimed to create value for the individual user — but we have seen from Big Tech’s practices that user-friendly design and public-friendly design are sometimes in tension with each other. Often, this user-centric orientation is directed towards contributing economic value (sometimes called “exchange-value” in economics).

With our work on the Public Spaces Incubator, we hope to design for not just individual value or business value in service of the sustainability of these institutions, but also public value. This is notoriously difficult to pin down — fields like economics, politics, and philosophy have been debating its definition for centuries. Moreover, as a recent report from the UCL Institute for Innovation and Public Purpose points out, there is an inherent tension in defining and measuring public value for many public service media organizations: on the one hand, they are expected to demonstrate public value through traditional consumption figures used by privately-owned media organizations such as advertising revenue, number of subscribers, or subscription revenue; on the other, they have public service mandates — to inform, educate, and entertain — that run counter to this for-profit logic.

One way to address this tension is to acknowledge that our work, co-designed with audiences, can create value across three dimensions: 1) for individual people, as users and citizens, 2) for public service media, as organizations and institutions, and 3) for the public at large. Alongside our collaborators, and grounded in our research with audience members, we have begun developing a framework to situate our objectives and measure the outcomes of our work along all three dimensions


https://www.ucl.ac.uk/bartlett/public-purpose/sites/bartlett_public_purpose/files/final-bbc-report-19_jan.pdf





## CIP whitepaper - value citation 

https://www.cip.org/whitepaper
I. Value elicitation: Given a set of possible directions for technology deployment, how might we aggregate, understand, and incorporate the conflicting values of overlapping groups of people? 

## Voting - eigenvoting 
https://www.plurality.net/v/chapters/5-6/eng/?mode=dark#fnref11
Correlation discounting and eigenvoting: QV and the Penrose rule apply degressive proportionality (using the the square-root rule) to the voting weights of respectively individuals and/or social groups (like nations). A natural extension would be to allow for a wider diversity of sources of correlation/coordination within and across individuals, as would be true in a general statistical model. In this case, an optimal rule would likely involve partial "correlation discounting" based on the degree of social connection and, perhaps, the identification of underlying


## Recommenders with values: developing recommendation engines in a public service organization - Structure 
https://knightcolumbia.org/content/recommenders-with-values-developing-recommendation-engines-in-a-public-service-organization


A typical architecture of recommender systems—see e.g., (Lada, Wang, & Yan, 2021) and (Google, 2020)—consists of a sequence where each subsequent step subsets or re-ranks a selection of content generated by the previous step:

Candidate generation: the system selects a set of candidate content items from a large corpus.
Ranking: the candidates are scored, ranked based on their scores, selecting a subset closer to the number of items which will be shown to the user.
Re-ranking/post-processing: a final post-processing step may be included to ensure the final set of recommendations fulfill some business criteria.


The effects of this feedback loop, where users discover and interact with content primarily through recommendations, has been called preference amplification: as users consume increasingly more recommended content, this is interpreted by the algorithm as a positive signal, leading it to surface even more content of the same type. This loop may likely narrow users’ interests toward the recommended content (filter bubble) and even reinforce their own existing views (echo chambers) (Kalimeris & Bhagat, 2021).

## AI and Practicing Democracy
https://ash.harvard.edu/resources/ai-and-practicing-democracy/

https://www.nber.org/system/files/working_papers/w32487/w32487.pdf
### Downstream Approach
A “downstream” approach focuses on how to use AI in a way that enhances democratic practice. For example, we have experimented with leveraging AI-assisted conversation analysis to coach leadership team meetings. Metrics of conversational share and turn-taking, can reveal, for example, that the supposed team “coordinator” is doing 80% of the talking, dominating more than leading. While conversation analysis is not unique to our context, the “heart challenge” of learning to intentionally engage tension and discomfort around power dynamics is a key part of learning to organize. We have found that, with the right pedagogical approach, data can productively scaffold engagement with such challenges, for example, enabling the coach to shift focus from the coordinator alone to engaging the team in collective reflection on how their interactions align with their agreed-upon norms. This is an example of what we call“evidence-based organizing,” a kind of AI-boosted “game tape” process, similar to how athletes use AI-assisted recording analysis to improve their performance. In the downstream approach, the key is to identify where AI can enhance existing craft, not replace it.

https://www.dpifund.org/resource-public/power-metrics-ec
### Upstream Approach
An “upstream” approach, in contrast, is primarily concerned with how to build AI. Training AI models to differentiate between “correct” and “incorrect” guesses is a crucial form of human influence, but how can we do this if we haven’t defined “correct” and “incorrect” from a democratic practice perspective? In research collaborations with the MIT Center for Constructive Communication and Elizabeth McKenna at the Civic Power Lab, we are exploring how to define the right metrics that differentiate between mobilizing, organizing, and governing power,11 and between values-based relationship-building and issues-based relational transactions.

Additionally, upstream approaches help us evaluate the potential limitations of AI models. Our research also explores whether large language models (LLMs) can be “taught” to recognize effective public narratives — a deeply emotional and relational leadership practice. The goal is not to replace human storytellers with machines but to recognize that algorithms have shaped our attention and behavior for years. This work asks how we might design algorithms that can recognize and prioritize values-based communication over marketing-oriented messaging, or whether LLMs might be missing something essential about human connection altogether.

Process it has meaning  People organize not just to move some coherent agenda forward. It is through organizing that we generate the democratic agenda, and in fact articulate, negotiate, and create the demos itself.

## Towards Graph Foundation Models: A Survey and Beyond
https://arxiv.org/pdf/2310.11829
(1) GNN-based
Models: They aim to enhance existing graph learning paradigms
through innovations in the backbone, pre-training, and adaptation
aspects; (2) LLM-based Models: They explore the feasibility of
using an LLM as a graph foundation model by converting graphs
into text or tokens; (3) GNN+LLM-based Models: They explore
various forms of synergy between GNNs and LLMs to empower
them with enhanced capabilities


Challenges about Applications
7.3.1 Killer Applications
In comparison to the outstanding performance of language foundation models in tasks like text translation [198] and text generation [199], whether graph foundation models can similarly
catalyze groundbreaking applications in graph tasks is not yet
clear. For scenarios that are well-suited for the application of
GNNs, such as e-commerce [82] and finance [200], potential
research directions include leveraging graph-based models integrated with LLMs to better support open-ended tasks [178],
or enhancing the reasoning capabilities of LLMs through graph
learning techniques [201]. Furthermore, graph foundation models
have the potential to make breakthroughs in some emerging fields.
For example, drug development is a time-consuming and costly
process [202], and language foundation models have already been
successfully used for related tasks like target identification and
side effect prediction [1]. Given the 3D geometric structure of proteins [203, 204, 205], graph foundation models hold the promise of
enhancing the drug discovery pipeline by leveraging their ability
to model graph structure information [206], potentially speeding
up the process further. Additionally, urban computing may also
represent a crucial application scenario for graph foundation models. It is worth noting that traditional traffic prediction techniques
have been primarily focused on addressing individual tasks such
as travel demand prediction [207] and traffic flow prediction [208],
lacking a comprehensive understanding of the entire transportation
system. Given that the transportation system can be viewed as a
spatio-temporal graph, graph foundation models hold the potential
to capture the participation behavior of actors in the transportation
system [209], thereby offering a unified approach to addressing
various issues in urban computing.
7.3.2 Trustworthiness
Despite the strong performance of LLM-based foundation models,
their black-box nature [210] introduces a host of safety concerns, such as hallucination and privacy leaks. The hallucination
refers to the output appearing plausible but deviating from user
input, context, or facts [211]. Existing research suggests that
this phenomenon is associated with multiple factors, such as
the model’s overconfidence in its own behavior [212] and the
misunderstanding of false correlations [213]. Similarly, recent
work has pointed out that pre-trained GNNs also pose certain
trustworthy risks about fairness [214] and robustness against
attacks [215]. Given the unique nature of graph data, we may
require certain techniques to prevent or mitigate security risks on
graph foundation models, such as confidence calibration [216] or
counterfactual reasoning [217]. Additionally, given that existing
research has indicated privacy risks in both GNN [218, 219] and
LLM [220], enhancing the privacy of graph foundation models is
also a critical concern. Some potential solutions include federated
learning [221], RLHF [61] and red teaming [222], but whether
these methods can be applied to graph foundation models is still
unknown.
8 CONCLUSIONS
The development of foundation models and graph machine learning has spurred the emergence of a new research direction, with
the aim to train on broad graph data and apply it to a wide
range of downstream graph tasks. In this article, we propose the
concept of graph foundation models (GFMs) for the first time, and
provide an introduction to relevant concepts and representative
methods. We summarize existing works towards GFMs into three
main categories based on their reliance on graph neural networks
(GNNs) and large language models (LLMs): GNN-based models,
LLM-based models, and GNN+LLM-based models. For each
category of methods, we introduce their backbone architectures,
pre-training, and adaptation strategies separately. After providing
a comprehensive overview of the current landscape of graph
foundation models, this article also points out the future directions
for this evolving field.

## GraphTranslator: Aligning Graph Model to Large Language Model for Open-ended Tasks
https://arxiv.org/html/2402.07197v4

3.3.Graph Question Answering (GQA)
To further reveal the potential and commercial value of our GraphTranslator across a wide range of open-ended applications, we showcase the graph question answering (GQA) experiments on Taobao dataset. We query the LLM in a multi-turn dialogue format to deeply investigate the capability of our GraphTranslator to extract, explain and reason the unseen node embedding.

To provide the quantitative analysis of GraphTranslator, we build an evaluation set by randomly sampling 100 nodes and constructing three questions as follows: (1) User Understanding: “Please summarize the user’s interests.” (2)Friends Understanding: “Please summarize the common interests and preference of these friends.” (3)Friendship Analysis: “Why does this user become friends with these people? ” For GraphTranslator  the translated user embedding is only concatenated with the first question, serving a soft prompt. As a comparison, we directly feed the text attributes of user and neighbors to ChatGLM2-6B. More details of prompts can be found in the Appendix D. As questions are open-ended, we employ both human volunteers and ChatGPT (GPT-3.5-turbo-16k) as the evaluators to perform quantitative analysis. Following (Wang et al., 2022), we gather question-answering pairs of each test sample and use the four-level rating system:

• Rating-A: The answer is correct and concise, the information is correct, and the reasoning is accurate.
• Rating-B: The answer is reasonable, with minor errors or imperfections.
• Rating-C: The answer is relevant to the question, but has obvious errors or inaccuracies in the content.
• Rating-D: The response is irrelevant or completely invalid.

PowerPoint of different algorithms: GNN, LLM, GNN + LLM 
https://www2024.thewebconf.org/docs/tutorial-slides/towards-graph-foundation-models.pdf 


Graph Convolutional Neural Networks for Web-Scale: Recommender Systems
Computation resources. Training of PinSage is implemented in
TensorFlow [1] and run on a single machine with 32 cores and
16 Tesla K80 GPUs. To ensure fast fetching of item’s visual and
annotation features, we store them in main memory, together with
the graph, using Linux HugePages to increase the size of virtual
memory pages from 4KB to 2MB. The total amount of memory used
in training is 500GB. Our MapReduce inference pipeline is run on
a Hadoop2 cluster with 378 d2.8xlarge Amazon AWS nodes.


4.2 Offline Evaluation
To evaluate performance on the related pin recommendation task,
we define the notion of hit-rate. For each positive pair of pins (q,i)
in the test set, we use q as a query pin and then compute its top
K nearest neighbors NNq from a sample of 5 million test pins. We
then define the hit-rate as the fraction of queries q where i was
ranked among the top K of the test sample (i.e., where i ∈ NNq).
This metric directly measures the probability that recommendations
made by the algorithm contain the items related to the query pin q.
In our experiments K is set to be 500.
We also evaluate the methods using Mean Reciprocal Rank
(MRR), which takes into account of the rank of the item j among
recommended items for query item q:

4.3 User Studies
We also investigate the effectiveness of PinSage by performing headto-head comparison between different learned representations. In
the user study, a user is presented with an image of the query pin,
together with two pins retrieved by two different recommendation
algorithms. The user is then asked to choose which of the two
candidate pins is more related to the query pin. Users are instructed
to find various correlations between the recommended items and
the query item, in aspects such as visual appearance, object category
and personal identity. If both recommended items seem equally
related, users have the option to choose “equal”. If no consensus is
reached among 2/3 of users who rate the same question, we deem
the result as inconclusive


4.4 Production A/B Test
Lastly, we also report on the production A/B test experiments,
which compared the performance of PinSage to other deep learning
content-based recommender systems at Pinterest on the task of
homefeed recommendations. We evaluate the performance by observing the lift in user engagement. The metric of interest is repin
rate, which measures the percentage of homefeed recommendations
that have been saved by the users. A user saving a pin to a board
is a high-value action that signifies deep engagement of the user.
It means that a given pin presented to a user at a given time was
relevant enough for the user to save that pin to one of their boards
so that they can retrieve it later.
We find that PinSage consistently recommends pins that are
more likely to be re-pinned by the user than the alternative methods.
Depending on the particular setting, we observe 10-30% improvements in repin rate over the Anno

## Stanford CS224W: Machine Learning with Graphs 
https://www.youtube.com/playlist?list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn

## ETA Prediction with Graph Neural Networks in Google Maps
• Innovations on how the road network data is featurised
and presented to the GNN;
• Innovations in the GNN model design and operation. While
the GNN itself is constructed of standard building blocks, we
found several benefits for the training regime (such as MetaGradients [31] and semi-supervised training [16, 26]) as well
as architectural ablations (e.g. carefully tuned combinations
of aggregators [5]) that proved particularly important for
maintaining stability of the GNN in this regime and making
it production-ready.
• Finally, we deploy the trained GNN model in production
within Google Maps, observing strong real-world benefits. As displayed in Figure 1, we noticed clear quantitative
improvements in negative ETA outcomes, but besides the
on-line performance, we performed several offline ablations
on various architectural and setup decisions, as well as visualisations of particular traffic situations where our model
has a clear advantage over the prior baseline.

RMSE


## Graph Neural Networks in Recommender Systems: A Survey - [Different GNN on the recommendation, will the relationship affect the recommendation - HP]
https://arxiv.org/pdf/2011.02260
Five typical GNN framework for the field of recommendation 
• GCN [73] approximates the first-order eigendecomposition of the graph Laplacian to iteratively
aggregate information from neighbors. Concretely, it updates the embedding by
• GraphSAGE [50] samples a fixed size of neighborhood for each node, proposes mean/sum/maxpooling aggregator and adopts concatenation operation for update,
• GAT [140] assumes that the influence of neighbors is neither identical nor pre-determined by
the graph structure, thus it differentiates the contributions of neighbors by leveraging attention
mechanism and updates the vector of each node by attending over its neighbors
• GGNN [89] adopts a gated recurrent unit (GRU) [89] in the update step

5 SOCIAL RECOMMENDATION
With the emergence of online social networks, social recommender systems have been proposed to
utilize each user’s local neighbors’ preferences to enhance user modeling [43, 65, 103, 104, 172]. All
these works assume users with social relationships should have similar representations based on
the social influence theory that connected people would influence each other. Some of them directly
use such relationship as regularizer to constraint the final user representations [65, 104, 105, 138],
while others leverage such relationship as input to enhance the original user embeddings [43, 103].
From the perspective of graph learning, the early works mentioned above can be seen as modeling
the first-order neighbors of each user. However, in practice, a user might be influenced by her/his
friends’ friends. Overlooking the high-order influence diffusion in previous works might lead to the
suboptimal recommendation performance [172]. Thanks to the ability of simulating how users are
influenced by the recursive social diffusion process, GNN has become a popular choice to model
the social information in recommendation.
To incorporate relationships among users into interaction behaviors by leveraging GNN, there
are two main issues to deal with:
• Influence of Friends. Do friends have equal influence? If not, how to distinguish the influence
of different friends?
• Preference Integration. Users are involved in two types of relationships, i.e., social relationships with their friends and interactions with items. How to integrate the user representations
from the social influence perspective and interaction behavior?

## Recommender Systems: The Rise of Graph Neural Networks
https://www.shaped.ai/blog/recommender-system-family-tree-gnn
Challenges and Future Directions
While GNNs have shown great promise in the field of recommender systems, there are still several challenges and future research directions to be explored:

Scalability: Developing efficient GNN architectures and training strategies is crucial to handle large-scale recommendation datasets. Techniques such as graph sampling, model compression, and distributed training can be investigated to improve the scalability of GNN-based recommenders.
Explainability: Designing interpretable GNN-based recommenders is important to provide insights into the recommendation process and build trust with users. Developing methods to explain the reasoning behind the recommendations generated by GNNs is an active area of research.
Diversity and Fairness: Incorporating diversity and fairness objectives into GNN-based recommendation models is essential to ensure balanced and unbiased recommendations. Techniques to promote diversity, mitigate bias, and ensure fairness in GNN-based recommenders need further exploration.
Temporal Dynamics: Extending GNNs to capture the temporal evolution of user preferences and item popularity is crucial in dynamic recommendation scenarios. Incorporating temporal information into GNN architectures and developing models that can adapt to changing user interests over time are important research directions.
Transferability: Investigating the transferability of GNN-based recommenders across different domains or platforms is valuable for improving their generalization ability. Techniques such as transfer learning and domain adaptation can be explored to leverage knowledge from one domain to enhance recommendations in another.

## DGRec: Graph Neural Network for Recommendation with Diversified Embedding Generation

However, a well-designed recommender system should be evaluated from multiple perspectives, e.g. diversity [49]. Accuracy can
only reflect correctness, and pure accuracy-targeted methods may
lead to the echo chamber/filter bubble [11] effects, trapping users in
a small subset of familiar items without exploring the vast majority
of others. To break the filter bubble, diversification in recommender
systems is receiving increasing attention. Through an online A/B
test, research [16] shows that the number of users’ engagements
and the average time spent greatly benefit from diversifying the recommender systems. Diversified recommendation targets increase
the dissimilarity among recommended items to capture users’ varied interests. Nevertheless, optimizing diversity alone often leads to
decreases in accuracy. Accuracy and diversity dilemma [50] reflects
such a trade-off. Therefore, diversified recommender systems aim
to increase diversity with minimal costs on accuracy [2, 5, 49].

Baselines. To empirically evaluate and study DGRec, we compare our model with representative recommender system baselines.
Note that DGRec is compatible with the re-ranking-based methods
such as DPP [5], MMR [4], DUM [2] and Diversified PMF [31]. Thus
we do not compare those methods in the experiments. Selected
baselines are shown as follows:
• Popularity: It is a non-personalized recommendation method
that only recommends popular items to users.
• MF-BPR [29]: It factorizes the interaction matrix into user
and item latent factors.
• GCN [18]: It is one of the most widely used graph neural
networks.
• LightGCN [14]: It is the state-of-the-art recommender system. LightGCN is a GCN-based model but removes the transformation matrix, non-linear activation, and self-loop.
• DGCN [49]: It is the current state-of-the-art diversified recommender system based on GNN.

4.1.3 Evaluation Metrics. Following previous works [5, 7, 49], we
use two different kinds of metrics to evaluate the accuracy and
diversity respectively. We aim to get a diversified item set during
the retrieval stage, so Recall and Hit Ratio (HR) are used to measure
the accuracy. Coverage is used to measure diversity, which counts
the number of covered categories of recommended items. To save
space, we only report Top-100 and Top-300 retrieval results. We
can reach the same conclusion for other top-N retrievals.

5.1 Graph Neural Network based
Recommender System
With GNN showing excellent performance on graph-structured
data, GNN-based recommender systems [34] are attracting more
and more attention. These methods represent the user’s historical
interactions as a user-item bipartite graph with easy access to highorder connectivity. GCMC [3] utilizes encoder-decoder structure
on graph to complete interaction matrix. SpectralCF [48] is the first
to study the spectral domain of the user-item bipartite graph. It proposes spectral convolution operation to find the latent interactions,
and greatly increase the recommendation performance on cold-start
items. PinSAGE [46] designs a special random walk to accelerate
the learning on the large-scale bipartite graph, which is applied
on the Pinterest platform. NGCF [37] directly aggregates information from neighbors in the bipartite graph, and explicitly injects
the collaborative signal in the learned embedding. LightGCN [14]
simplifies NGCF by removing the overhead computation of linear
transformation and non-linear activation. The simplified operation
not only achieves better performance but also reduces the training time. UltraGCN [25] takes a further step in simplifying graph
convolutional network. It skips the finite layers of aggregation, and
directly computes the infinite convolution stage as a constraint
during training. MetaKRec [43] reconstructs the knowledge graph
as edges between items before graph convolution.
Previous GNN-based recommender systems nearly all focus on
increasing accuracy while leading to poor diversity. DGRec is also
built upon Graph Neural Network. The proposed three modules
can be added to previous GNN-based recommender systems and
make up for their diversity shortcomings.

## Fine-tuning language models to find agreement among humans with diverse preferences 

https://www.semanticscholar.org/reader/de1c7ae2818aa26fc86a0ea8ed70014cffc8b20a

## Persuation - fake news 

## AI moderator in the group 

## Elicitation Inferece Optimization for multi-principal-agent alignment 
https://openreview.net/pdf?id=tkxnRPkb_H

## Democratic Policy Development using Collective Dialogues and AI 
https://peacepolls.etinu.net/peacepolls/documents/009674.pdf

## "Generative AI" through collective response systems
https://arxiv.org/pdf/2302.00672

## Measuring Deliberation Measuring Deliberation2.0: Standards, Discourse Types, and Sequenzialization1
https://ash.harvard.edu/wp-content/uploads/2024/02/baechtiger_0.pdf

## A formmal theory of democratic deliberation 
https://www.cambridge.org/core/journals/american-political-science-review/article/formal-theory-of-democratic-deliberation/78A6828E834595C799DB4103C1C7976B?utm_source=chatgpt.com

## Rethinking Fair Graph Neural Networks from Re-balancing
https://arxiv.org/pdf/2407.11624

## Graph Machine Learning in the Era of Large Language Models (LLMs)
https://arxiv.org/html/2404.14928v2

## Bridging Systems: Open problems for countering destructive divisiveness across ranking, recommenders, and governance
An allocation system (or simply allocator) is a process that determines which of many potential allocations will actually occur, taking as input a set of potential allocations and outputting a set of realized allocations.

set of potential allocations -> value model -> selection 
impact prediction (e.g. engagement, knowledge, harm, entertainment) 
value model (can incorporate the bridging impact) 
selection [value optimization] - realized allocations 





