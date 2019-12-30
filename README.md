# Generate-TV-Scripts
Udacity RNN Deep Learning Nanodegree Project

Original repo for this project can be found [here](https://github.com/udacity/deep-learning-v2-pytorch/tree/master/project-tv-script-generation).

## Objective
In this udacity project, I have generated my own Seinfeld TV script using RNNs from using a part of the [Seinfeld dataset](https://www.kaggle.com/thec03u5/seinfeld-chronicles#scripts.csv) of scripts from 9 seasons. The Neural Network I built, generates a new ,"fake" TV script, based on patterns it recognizes in this training data.

## Steps
- preprocess the data
- batch the data
- build the RNN
- train the RNN
- generate tv script

## Results
- the LSTM-generated text cannot create long-term meanings yet
- I obtained a training loss lower than 3.5
- I trained the RNN for 10 epochs using a learning rate of 0.001
- I intially tried a sequence length higher than 10 but I found out that with a sequence length of 10, the model converges faster
- I chose a batch size of 128, since smaller sizes have more noise in their error calculations which is helpful in preventing the training process from stopping at the local minima
- I decided the number of hidden dimensions (250) so that the model does not overfit
- For character level language modelling, a depth of at least 2 layers for RNN is known to be beneficial so I went for n_layers = 2

## Sample from the Generated Tv script

> elaine: required like a woman, but the whole concept of our solar sentences a good thing.
>
> george: i don't know...
>
> george: oh, no! classic, that's not the way to go to your apartment.
>
> george:(confused) i think i should have to get going. i mean...
>
> jerry:(to kramer) you don't know how to say?
>
> elaine: yeah!
>
> jerry: i can't believe this.
>
> jerry:(looking at george) hey.
>
> elaine: hey, i got the job interview. i can't even get the call. you got that rye.
>
> jerry: what? i mean, you think i was a little kid.
>
> elaine: oh, no. no, no no no no no. i don't know, you can be a good thing.
>
> elaine: oh, no- no no no.. no.
> 
> kramer:(to jerry) i guess i can have lunch with this. i think i can do that!
> 
> elaine: what?(to the cashier) oh yeah, you got it.
>
> elaine: i thought you were in.
>
> jerry:(to jerry) you know what i said?"
>
> kramer: oh yeah, i think i should go to my head....
>
> jerry: yeah! karate! 's off! eats it! air! pilot! 's off! air."
>
> kramer:" so what are you gonna do?
>
> elaine:(laughing) i don't know.
