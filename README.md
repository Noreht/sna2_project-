# Analysis of 2017 US Congressional tweets to establish levels of bipartisanship across different key US electoral issues
Theron, Quinn, Kaya (Xinyi Wu) , Yujin, Cherie & Ivy (Yu Wang)


 
## Introduction
In the current landscape of American politics, characterized by deep partisan divides, many pressing political and social issues persist in need of resolution. Under this situation, do the two major parties in the United States engage in cooperation, focusing jointly on common concerns, or do they remain divided, each acting with their own agendas? How do  differing political affiliations impact the attention politicians devote to similar societal issues and their overall political attitudes? And how is this reflected in online interactions between US congresspeople?
To investigate these questions and explore how political stances influence bipartisan discussion on key societal matters, our group has undertaken an analysis of Tweets by members of the 115th US Congress. Specifically, we aim to establish levels of bipartisanship across different key US electoral issues by examining a dataset of tweets from August 2017. Through an examination of the interconnectivity and topical focus of tweets from congress members of both parties, we seek to understand which styles of discussion are politically divisive and which are bipartisan. More specifically, we have selected three long standing issues—health, military affairs, and immigration—that have garnered sustained attention. Through our analysis, we hope to gain an understanding of the relationship between the two major parties, the Republican party and the Democratic party, in the United States during the 2017 period.

## Methodology
Our methodology began with the acquisition of tweets from members of Congress for August 2017, sourced from alexlitel’s Tweets of Congress database. For our first step, we extracted the accounts of Congressional members from the database and coded them as red (Republican) and blue (Democrat). For the two independent members, we manually assigned them as Democrats, since they both caucused with the Democratic Party in the Senate. 

Next, we identified relevant keywords related to health, military affairs, and immigration through combining relevant news with the tweets' content. We parsed the tweets to identify those containing these keywords that are related to our area of interest. We then constructed a bipartite graph with nodes representing both politicians and keywords, and edges connecting politicians to the keywords present in their tweets. Using the Louvain algorithm, we identified distinct “communities” of discourse, representing clusters of politicians and keywords that frequently co-occurred. We assessed bipartisanship within each community by analyzing the proportion of politicians from different parties and the frequency of the appearance of relevant keywords that we have selected. 

Our quantitative analysis involved calculating metrics such as modularity and clustering coefficient to evaluate the structure and cohesion of the identified communities. Meanwhile, qualitative analysis of the content and context of tweets within each community helped identify recurring themes and patterns of bipartisan or partisan discourse. We compared the composition and characteristics of communities across different political and social issues to discern variations in bipartisanship levels and the level of attention of different political parties on the same issue. Finally, we synthesized the results to generate comprehensive insights into bipartisanship levels across different issues. 

### Immigration

To capture congressional Twitter discourse on immigration, we conducted an initial keyword search that included inflammatory terms such as "rapist", and "border." This was done intentionally to ensure that we included extreme rhetoric relevant to the discussion. Many of these terms had been popularized by then-president Donald Trump during his 2016 campaign, which we felt warranted their inclusion.

Once we completed our keyword search, we sorted our remaining tweets using the Louvain algorithm to identify "communities" of discourse. We then sorted the members of each community by party affiliation to better understand the proportion of Democrats to Republicans within them. 

![newplot](https://github.com/Noreht/sna2_project-/assets/151726759/ff2d78f3-f347-4f4f-81d3-b83777a86f9f)

We repeated this same process to identify communities of discourse on healthcare and the Military.

### Healthcare

![newplot-2](https://github.com/Noreht/sna2_project-/assets/151726759/6c0c531b-dc48-4d73-9257-eae050d80746)

### Military

![newplot-3](https://github.com/Noreht/sna2_project-/assets/151726759/9ad3c7a0-ab88-40f0-9402-2bc966cae750)


## Analysis

### Immigration

Perhaps our most surprising finding was the results returned by our analysis of communities on immigration. Even after including extreme language to account for the tougher stance that Republicans have taken on immigration, it was still Democrats who appeared more often in our results. This might indicate a disparity in the importance of immigration as an issue of government for Democrats and Republicans. Since the Congress had only been sworn in 8 months ago, this might indicate that the issue of immigration mattered more to Republicans as an election issue and not a government one. A list of the most commonly used words in each community is included below.

<img width="440" alt="Screenshot 2024-05-17 at 10 50 10 AM" src="https://github.com/Noreht/sna2_project-/assets/151726759/78aa0ac5-c6f3-4ca6-9427-44e0086413e3">

### Healthcare

Perhaps unsurprisingly, Democrats tended to dominate the discussion surrounding healthcare, as healthcare reform or renovation in some form has been a core component of the Democratic platform for some time. 

<img width="443" alt="Screenshot 2024-05-17 at 10 53 21 AM" src="https://github.com/Noreht/sna2_project-/assets/151726759/a3432cbc-1f4f-4b4c-8f38-c16915cb8f2d">

### Military

Both Democrats and Republicans engaged with each other rather frequently in discussions of the military. At the same time, it appears that Democrats were more outspoken regarding issues related to Veteran's health.

<img width="439" alt="Screenshot 2024-05-17 at 10 54 47 AM" src="https://github.com/Noreht/sna2_project-/assets/151726759/0f22fd6b-ac3a-4dfb-a025-60a3794090d5">

## Limitations and Improvements
Our analysis yielded bar graphs visualizing political representation and community engagement, but we also acknowledged several limitations. 

First, our results are highly dependent on the keywords selected, significantly influencing which tweets are included and potentially omitting relevant discussions. Our personal bias during the word selection phrase may also lead to the imperfection of the list of words, leaving the subsequent investigation with certain deviations.

Second, the Louvain algorithm we used sorts tweets into a single community, which means that tweets potentially belonging to multiple subject areas are only placed in one, misrepresenting the multidimensional nature of some discussions. 

Additionally, our dataset which consists of tweets from only one month in 2017 is relatively small and outdated. Running the same process today would likely bring different results due to changes in political discourse and new developments in key issues. Furthermore, our definition of community focuses solely on the interactions of Congress members, which does not represent the broader discourse that includes public opinion, media, and other stakeholders.

To address these limitations and enhance the robustness of future analyses, several improvements could be made.
Expanding the dataset to include tweets from a longer period and updating it to include recent data would provide a more comprehensive and current view of political discourse. Using more sophisticated methods for keyword selection, such as dynamic topic modeling or expert consultation, could ensure a more accurate capture of relevant tweets. Implementing a multilayer community detection algorithm would allow tweets to belong to multiple communities, better reflecting the complexity of political discussions. Extending the analysis to include interactions with the public, media, and other political entities could provide a more holistic view of the discourse and how it influences and is influenced by Congress members. 

Finally, we originally wished to use Natural Language Processing (NLP) to identify the sentiment of tweets, which would help discern whether Congress members intended to collaborate or held opposing views on the same issue. However, due to the limited data from just one month, this was not feasible. Acquiring a larger dataset would enable us to utilize NLP techniques effectively, providing deeper insights into the attitudes and potential for collaboration among Congress members.


## Conclusion
At a time when US politics appear more divided than ever in recent memory, finding spaces of bipartisan discussion becomes that much more important. Understanding how politicians across the political spectrum and from both major parties interact online can help us to understand where consensus on long standing political issues may lie. Our analysis indicates that while some spaces of consesus were built between Republicans and Democrats on Twitter, there remains a substantial difference in how both parties and its members choose to discuss the same topics. With more time and a larger dataset, it may become possible to chart how this discourse has shifted over time since 2017.

