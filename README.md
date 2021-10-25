# Portfolio
Welcome to my portfolio, i'm Adil Qarboua a new technologies ethousiast, i have strong interest to the fields of Artificial Intelligence and High Performance Computing.
i have a preference towards low level programming language (C and C++) as i awkwardly feel like not doing too much when i use Python.

In the next sections i will present my academic background with emphasis on two particular projects.

I hope that you will find it interesting.

## Precedent work
### C/c++
<details markdown=1>
  <summary> Hypergraph Embedding for Clustering</summary>
  
  #### Introduction
  
  _Graph embedding_ is a method who tries to **transform graph nodes to vectors** representing theese nodes.
  The vectors should capture some of the caracteristics of the nodes mainly their **proximity**.
  Two nodes who are neighbors should be embedded to two vectors having a low distance measure (Euclidian Distance for example) between them.
  
  #### Application  
  Graph embedding have a large application panel like :
 
  * Biomedical and BioInformatic
  * Association Rule 
  * **Features encoding** 
  We will focus on features encoding. In the next section i will present the principle of Word2Vec who is widely used on NLP and who is
  mainly based on graph embedding.
  
  #### Word2vec and auto-encoders
  Word2vec is an algorithm who process a text corpus and who transform each word into a vector based on the training of a special
  type of auto-encoders.
  
  A classic auto-encoder is a neural network where the labels (the output desired vectors) are the input data.
  The goal of an auto encoder is to capture the input vectors on the weights at the middle hidden layer.
  It's used for compression purposes by feeding a neural network where this layers contain less nodes than the original vectors dimension.
  
  ![an auto encoder]()
  
  The special type of auto-encoders used by Word2vec is called a skip-gram model where the desired are the words who appears in the same
  context.
  
  Word2Vec work by assuming a relatively coherent hypothesis wich is **two words who appears on the same context may have the same signification**.
  
  Let's take a look on a funny equation involving words instead of numbers.
  
  Paris - France + England = London.
  
  Even if it's not common it's seems correct we can interpret it as if you retrieve the signification of  the word France from the word Paris you will end up with 
  Capital city by adding england to it you end up in London.
  
  In reality the text corpus this particular skip gram model was trained on is a corpus who describe different statistic metrics on cities. Paris and London appears often on the same context as (The highest population density, The highest GPD per capita etc...).
  The fact that words where transformed into vectors allow us to do the - and + operations and the equality (the = operator) is in reality the word represented by the vector with the lowest euclidian distance to the current result of the equation.
  
  How can a skip gram model capture this proximity regarding to the context?
  
  Take a look at the next figure.
  ![a skip gram model]()
  
  The skip garm model will train an auto encoder as if the most common desired output for each word is the most common words surrounding it on a sentence.
  Two words will be similar (have a low euclidian distance between them on the vectorial space) if they appear often on the same context.
  
  The auto encoder duty will be to encode sufficiently well the input vector on the most inner hidden layer of it's encoder part.
  
  So if you retrieve the weights of this layer they should somehow encode the features in a way that will allow a discrimination,
  these weight will then represent the features on the vectorial space after the training.
  
  #### Clustering and similarity
  During this section i will briefly present the principles behind the clustering algorithms present on the figure Clustering algorithm and similarity.
  Then i will present Hashian and Liu Hypergraphs modelisation proposal for capturing similarity between features of a qualitatif dataset based on frequency.
  #### DeepWalk, Node2Vec and Random Walks
  During this section i will present the way i implemented Node2vec and Deep Walk for hypergraphs embedding purposes.
  #### Results
  I will present the result on 2 real datasets. A dataset of AliBaba clients who tries to identify wich incentives (ticket reduction, Proximity of stores) affect customer fidelity.
  A dataset of patients diagnosed with laro-pharynx cancer who tries to identify the common traits of these patients.
  
</details>
  
