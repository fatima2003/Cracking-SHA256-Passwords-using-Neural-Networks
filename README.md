# Cracking SHA256 Passwords using Neural Networks

This idea has been on my mind for the last 2 years but I couldn't find a simple enough research answering this question. I decided to take matters into my own hands. 

### Idea
The goal of this experiment is not to find a perfect model predicting the whole password from its hash and vice versa, but rather just using the first few bits of the hash to predict the password. This logic is skewed in that the first few bits of any good hashing algorithm (like SHA256) have/should have no direct correlation to the first few bits of the password itself. But my wonder cannot be satisfied by mere mathematical proof. 

### Dataset
10,000 common passwords: https://www.kaggle.com/code/shivamb/10000-common-passwords

### Progress
I used the first 4 bits of the password and hash with a test:train split of 0.2 and got:

###### Loss 2.4686e-09 

###### MAE 2.4580e-05

###### Test MAE 2.4125338313751854e-05

### Progress
These results are considered pretty good but the validity of the experiment is questionable. I will be trying to increase the number of bits from the password and hash and repeat the experiment with different hyper parameters.
