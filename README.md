# My_PyTorch

### Common PyTorch `mistakes`:
1. Didn't overfit a single batch (run your model on a single batch/example and make sure it is overfitting)[make sure no bug and network is in a good shape]
2. Forgot to set `training` or `eval` mode[for validation/test, it must set to eval to avoid dropout and batch normalization]
3. Forgot `.zero_grad()`[sequence: 
   + optimizer.zero_grad()
   + loss.backward()
   + optimizer.step()]
4. Softmax with CrossEntropyLoss (CrossEntropyLoss already means SoftMax + Negative Log Likelihood, so we should avoid applying SoftMax before CrossEntropy)
5. Using `bias` when using BatchNorm
6. Using view instead of permute for Transpose(to get transpose we have to `x.permute(1, 0)`)
7. Using bad data augmentation(for exmaple augmentation may affect the label (ornegin ters donmus bir 2 image'nin faydasi yoktur)
8. Not `suffling` data
9. Not `normalizing` the data
10. Not clipping gradients when using LSTMs, RNNs, GRUs


 
