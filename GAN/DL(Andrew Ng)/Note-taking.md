## GDSC
# 1. Introduction to Deep Learning    
***
#### AI=Electricity       
* effecting almost every industry    

#### What is a Neural Network?   
* single neuron : x --(node-function)--> y       
* multi neurons : x1, x2, ... xn --(nodes-functions)--> y    

* Neural Network :    
  - every features are connected to every nodes(first layer)    
  - nodes(hidden units) and functions each(ex RELU)    
  - *given enough train sets, NNs are remarkably good at figuring out (activtation)functions* that accurately map from X to y    
  - powerfull in Supervised learning    
  
* Supervised Learning    
  - Xs, Ys and Applications    
  - examples    
    + Standard NN(nodes and funcs0    
    + Convolution NN(images etc)    
    + Recurrent NN(sequentail data like nlp etc)    
  - Data    
    + Structured Data : each features have very well-defined meaning    
    + Unstructured Data(Audios, Images, Text etc) : features are pixels, individual words    
      + compared to Structured data, humans have evolved to be good at interpreting *unstructured data*    
      + thanks to NN, computers are now much better than few years ago    
    - Still, economic benefits come from Structured data actually    

* Drivers of DL    
  1. Increased Scale    
    - Scales of Performance for the Amount of data    
      1. Traditional learning alog(SVM, LR etc) : limit to the increase(turns to horizontal increments)    
        + don't know what to do with huge amounts of data from nowadays    
      2. NN : as more and more data is put, performance keep gets better and better    
      -> In order to increase performance, NN *needs a lot of LABELED data* and *a big size(hidden units+parameters+connections)*    
      + If small training sets, there isn't and order between 1 and 2    

  2. Increased computation    
  
  3. Improvement of Algorithms    
    - Gradient Descent got faster changing Sigmoid -> RELU    
      + Sigmoid : slow training regions where gradients are almost zero    
      + RELU(Rectified Linear Unit) : gradients equal to 1 in all part of the input, so it doesn't gradually head to zero(rather momentarily)    


  - with 2 and 3, training time reduced from 1 months to 10 mins, days(not always) so it became much more likely to discover NN that works well for applications    
  
***

# 2. Basics of Neural Network Programming    
***
#### Binary Classification      
* Image
  - pixel(c*r)* 3(rgb)
  - 0 or 1
  - Sigmoid( -infinite approximit 0, infinite to 1)
    + y(z)=1/(1+e^(-z))

#### Logistic Regression Cost Function
* Loss (error) function : measures how good our y_hat is compared to y(true label)(single training example)
  - doesn't work well in GD
  * L(y^, y)=-(ylogy^+(1-y)log(1-y^))
  * if y=1 : L(y^, y)=-logy^ (y^ large)
  * if y=0 : L(y^, y)=-log(1-y^) (y^ small)
* Cost function : measures how good our w, b are doing in our entire training example
  * J(w, b)=1/m(sigma L(y^, y))=-1/m(sigma ylogy^+(1-y)log(1-y^))

#### Gradient Descent
* train parameters w and b
* finding w and b which makes J(w, b) as small as possible(b is dimension)
* w := w - a * dJ(w, b)/dw
* b := b - a * dJ(w, b)/db

#### Computation Graph
<img src="https://user-images.githubusercontent.com/68985625/134808546-0085f341-dc06-4118-8b12-fc4dd5bd2054.png">



***










