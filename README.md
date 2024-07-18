# Detecting-Fake-News-on-Social-Media-Using-Graph-Neural-Networks-GNNs-

## Introduction
In today’s digital age, the rapid proliferation of information on social media platforms has significantly complicated the task of distinguishing authentic news from deceptive misinformation. This
paper delves into the application of sophisticated machine learning strategies, specifically Graph
Neural Networks (GNNs), to tackle this issue. Utilizing the UPFD dataset—a comprehensive collection featuring detailed propagation networks of both fake and real news items on Twitter, authenticated by reputable sources such as Politifact and Gossipcop—this study aims to decipher the
complex diffusion patterns that characterize the spread of misinformation. The dataset includes rich
node representations derived from nearly 20 million tweets, offering a substantial foundation for
not only understanding but also effectively countering the dissemination of fake news. Through a
methodical analysis, this research explores how GNNs can leverage these vast data points to detect
and mitigate the impact of false information, providing insights into the dynamics of news spread in
social media ecosystems.

### Abstract
The prevalence of fake news on social media is a growing concern, posing significant challenges to
information veracity online. This study employs Graph Neural Networks (GNNs) to detect and analyze the spread of fake news using the UPFD dataset, which contains verified propagation networks
of fake and real news on Twitter. The dataset, verified by sources like Politifact and Gossipcop, encompasses detailed interactions from nearly 20 million tweets, providing a granular view of how information, both true and false, proliferates across social networks. By applying GNNs, this research
highlights the potential of advanced machine learning techniques in recognizing and understanding
misinformation patterns, thereby aiding in the development of more robust systems to combat fake
news. The findings demonstrate the effectiveness of GNNs in parsing complex network structures
and offer valuable insights into the mechanisms of news distribution on social media, suggesting
pathways for both technological and informational interventions.

#### Architecture
Graph neural networks (GNNs) detect fake news by leveraging the relational data inherent in social
media networks, where nodes represent users or articles and edges signify interactions like retweets
or shares. In practice, GNNs initiate by embedding articles and user profiles into high-dimensional space using pretrained models like BERT for textual content and node-specific metadata for user
activities. The GNN layers then perform iterative aggregations of these features across the network’s
topology, where each node’s updated state is a function of its neighbors’ features, weighted by the
edges connecting them.
This aggregation may incorporate attention mechanisms, allowing the model to learn which connections (e.g., user interactions) are most indicative of misinformation spread. For instance, a GNN
can assign higher importance to edges connecting nodes frequently involved in spreading fake news.
Once the network aggregates features through several layers, the final node embeddings capture not
just individual article or user characteristics but also contextual information reflecting their broader
network role. The proposed model architecture employs a sophisticated multi-component strategy to
discern the authenticity of news articles by analyzing both their content and the surrounding social
context. Below, we outline the key components of the model:

1. Social Context Extraction: This stage utilizes a Graph Neural Network (GNN) to derive embeddings that capture the dynamics of user interactions, such as likes and shares,
providing insights into the social spread of news.

3. Endogenous Preference Encoder: Leveraging advanced text representation techniques,
this encoder transforms news content into embeddings that reflect textual features, offering
an understanding of the content independent of social interactions.

5. Exogenous Context Encoder: Integrates embeddings from user preferences and news
content with those from social contexts, resulting in a comprehensive representation that
encompasses both textual and relational information.

7. Neural Classifier: Receives combined embeddings and applies a classification mechanism
to determine the news’ authenticity, categorizing each piece as real or fake.

9. Loss Function: Utilized during training, this function optimizes the model to minimize
discrepancies between predicted and actual labels, enhancing the detection accuracy.

For classification, these embeddings are fed into a softmax layer, predicting the likelihood of news
being fake or real. The training process involves optimizing these predictions against a known
dataset of labeled news items, using loss functions that penalize discrepancies between predicted
and actual labels. By training on diverse examples of news propagation, GNNs learn to identify
subtle patterns and structures typical of fake news dissemination, making them effective for realtime detection on evolving social media platforms.
