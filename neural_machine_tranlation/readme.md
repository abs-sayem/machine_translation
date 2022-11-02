## **Neural Machine Translation**
###### **Neural Machine Translation is a special area of NLP, defined as the act of translation with the help of an artificial neural network. Here, we will learn about:**
* How Neural Machine Translation works
* NMT by jointly learning to align and tranlate
* Attention based NMT
* The dataset we will use

#### **Configuring the Environment**
###### **We need to have the Tensorflow and Tensorflow Text library installed in our system. Both are pip-installable:**
* `pip install tensorflow`
* `pip install tensorflow-text`

#### **Probabilistic Overview of NMT**
###### **Before go further lets have a look on probability basic. `P(X|Y)` refers to a probability of the event `Y` occuring given `X` has occured.<br>Now imagine `B` and `E` as asequence of Bangali and English words, respectively. If we apply the same difination of conditional probability here, it will mean `P(B|E)` is the probability of a sequence of words in Bangali `(B)` occuring, given there is a sequence of words in English `(E)`.**