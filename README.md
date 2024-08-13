# Cracking SHA256 Passwords using Neural Networks

This idea has been on my mind for the last 2 years but I couldn't find a simple research answering this question. I decided to take matters into my own hands. 

### Idea
The goal of this experiment is not to find a perfect model predicting the whole password from its hash and vice versa, but rather just using a few bits of the hash to predict (part of) the password. This logic is skewed in that the a few bits of any good hashing algorithm (like SHA256) have/should have no direct correlation to a few bits of the password itself. But my wonder cannot be satisfied. 

### Dataset
10,000 common passwords: https://www.kaggle.com/code/shivamb/10000-common-passwords

### Progress
I used the first 4 bits of the password and hash with a test:train split of 0.2 and got:

###### Loss 2.4686e-09 

###### MAE 2.4580e-05

###### Test MAE 2.4125338313751854e-05

### Progress
These results are pretty good but the validity of the experiment is questionable. Futher research shows that the first few bits are padding hence the low loss.
