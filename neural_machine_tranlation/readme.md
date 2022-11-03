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
###### **That means the task of translation (from Bangali to English) is to maximize this probability `P(B|E)`. The neural network's task is to larn the conditional distribution, and then when a source sentence is given, search for an appropriate target sentence by maximizing this conditional probability.**

#### **Math Behind NMT**
###### **NMT is the process of leveraging an artificial neural network to maximize this conditional probability.<br>An NMT architecture usually comprises an encoder and a decoder. Before `Bahdanau` and `Luong`, the encoder and decoder used only recurrence to solve the machine translation task. Here, we will discuss the math behind modeling translation using only RNNs as encoder and decoders.<br>Lets consider the equation of the hidden state of the RNN in the encoder:**
###### $$h_t = f(x_t, h_{t-1})$$
###### **Here, `f` is a neural network (can be an RNN, LSTM or GRU). The main motivation here is to understand that the current hidden state `$(h_t)$` depends on the current input $(x_t)$ and the previous hidden state $(h_{t-1})$.**