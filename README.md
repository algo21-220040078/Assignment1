# Assignment1
Basic Thoughts
===
For this assignment, I mainly use Back Propagation Neural Network method to predict the future return rate of private equity funds. I choose BP because the fluctuation of private equity fund shows strong nonlinear characteristics. And because of the data scarcity, the studies of related content of private equity fund prediction in China market are few. Meanwhile, the neural network requires a large sample size of the data.

Data Source
===
Sample data are from the CHFDB database. The period of data is from the January of 2015 to the December of 2019. It contains 258 weeks.

Data Processing
===
Input and Output
---
We select eight variables which have greater influence to the objective and have the less correlation between each other.![输入输出](https://user-images.githubusercontent.com/80868998/111778196-43bdb700-88ef-11eb-83d7-ee6748fccbee.png)
Data Normalization
---
Training Methods
---
According to the principle of 8:2, the training set and the test set are divided. The data of the first 205 weeks are used to training set and the remaining 53 weeks are used to test set. We use the data of 205 weeks to forecast the return rate of the 206th week. And then to forecast the 207th return rate until the 258th week.
Structure
---
We choose a three-layer feedforward neural network structure containing an input layer, an output layer and a hidden layer. We use S hidden layer and linear output layer to realize the output. It was found that 10 neurons have the best prediction effect.
Training Numbers
---
We use the mean square error as the loss function, Adam as optimizer and the learning rate is 0.01. When the epoch is 30, MSE is the minimum and the epoch is determined to be 30.![损失函数](https://user-images.githubusercontent.com/80868998/111780263-1de5e180-88f2-11eb-8ba5-4b3110357461.png)
Conclusion
===
![实际和预测图](https://user-images.githubusercontent.com/80868998/111780549-81700f00-88f2-11eb-9a3e-415aaf10a22c.png)
Although the overall trend is similar and the last seven weeks are very consistent, most of them misjudge the increase in returns as a decrease in returns. Investors are likely to lose higher potential future returns if they make decision according to this.
The prediction of BP neural network model is more accurate in the period of serious loss and the loss value is more extreme. From this point of view, BP neural network model is helpful for investors to avoid potential huge losses in the future.
