# Introduction

## What data is used for this project?

In the following, a data-set from [Wanjia et al. (2021)](https://www.nature.com/articles/s41467-021-25126-0#citeas) that is available on [OpenNeuro](https://openneuro.org/datasets/ds003707/versions/1.0.0) will be used. The goal is to assess if a machine learning algorithm trained on the `old` vs `new` images is able to predict the activity on subsequent 
images. Thus, the question is, with what precision will the algorithm be able to predict if a picture has been previously studied or not. 

The data-set will be explored witin the [data-exploration section](https://tchaase.github.io/research-internship-2022/code/data_exploration.html). Here, the idea is mainly to oultine the idea behind the research question. 

The primary goal of the authors of the original study was to answer a very different question than the one pursued here. Wanjia et al. were interested in how the brain activity changes in relation to highly similar images. They wanted to show, in what way a decorrrelation of hippocampal activation may relate to a subsequent resolution of memory interference. In their study, the authors were able to show that activity in the regions of the dentate gyrus and one subregion of the hippocampus (CA3) show a decorrelation pattern that is associated with learning. While memories traces that interfere will overlap during the initial encoding, over time the authors found there to a pattern that leads to these memory traces being less similar, therefore aiding memory performance. 

In the present study, the design of the study described above will be used to pursue answering a very different question. How well can machine-learning be used to classify brain activation for the classic old-new recognition paradigm.

## The old-vs-new paradigm

Let's take a look on what ChatGPT would answer when we ask it to provide us some information on the old-new paradigm (ChatGPT, personal communication, 2022, March the 5th)
<blockquote>
<p> Several studies have examined the neural correlates of old-new recognition using fMRI. For example, some studies have found that successful old-new recognition is associated with increased activity in the medial temporal lobe (MTL), including the hippocampus and parahippocampal gyrus, which are known to be important for long-term memory formation and retrieval (e.g., Davachi et al., 2003; Eldridge et al., 2000).

Other studies have focused on the role of the prefrontal cortex (PFC) in old-new recognition. The PFC is thought to play a critical role in monitoring and manipulating information in working memory, which may also be important for successful old-new recognition. For example, some studies have found that successful old-new recognition is associated with increased activity in the dorsolateral prefrontal cortex (DLPFC), which is thought to be involved in working memory processes (e.g., Ranganath et al., 2000; Simons et al., 2005).

Overall, the literature suggests that successful old-new recognition is associated with activity in both the MTL and PFC, which may reflect the complementary roles of these regions in long-term memory formation and retrieval. </p>
</blockquote>

In the following, I will outline what this paradigm is about and what we can expect, diving into the literature that ChatGPT recommended. 

## What can we expect from the previous literature?

Differentiating what we have previously seen from what we have never encountered is a skill we rely on in various areas of our every day life. This ability is inherent to our memory, as apart of which we are able to *encode*, *store* and *retrieve* information ([Melton, 1963](https://www.sciencedirect.com/science/article/pii/S0022537163800638)). Even though this ability is remarkable, it has only been in the recent years that human-kind has began to unravel how our memory function and how it is implemented on the neuronal level ([Tulving, 2002](https://www.annualreviews.org/doi/full/10.1146/annurev.psych.53.100901.135114?url_ver=Z39.88-2003&rfr_id=ori:rid:crossref.org&rfr_dat=cr_pub%3Dpubmed&)). 

Different areas of the brain are known to be important for the ability to recognize what was previously seen, i.e. `recognition memory`. 