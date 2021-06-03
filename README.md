# Portfolio
A simple presentation

## Precedent work
### C/c++
<details markdown=1>
  <summary> Hypergraph Embedding</summary>
  
  #### Introduction
  
  _Graph embedding_ is a method who tries to **transform graph nodes to vectors** representing theese nodes.
  The vectors should capture some of the caracteristics of the nodes mainly their **proximity**.
  Two nodes who are neighbors should be embedded to two vectors having a low distance measure (Euclidian Distance for example) between them.
  
  #### Application  
  Graph embedding have a large application panel like :
 
  * app1
  * app2
  * **Features encoding** 
  We will focus on features encoding. In the next section i will present the principle of Word2Vec who is widely used on NLP and who is
  mainly based on graph embedding.
  
  #### From Word2vec to classification using hypergraphs
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
  
  In reality the text corpus this particular skip gram model was trained on is a corpus who describe different statistics on cities. Paris and London appears often on the same context as (the capital city , the highest population density etc...).
  The fact that words where transformed into vectors allow us to do the - and + operations and the equality (the = operator) is in reality the word represented by the vector with the lowest euclidian distance to the current result of the equation.
  
  How can a skip gram model capture this proximity regarding to the context?
  
  Take a look at the next figure.
  ![a skip gram model]()
  
  .
  
  
  
  
  
  
  
  
  
</details>
  
