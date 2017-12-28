list of papers and summaries

1. Intriguing properties of nueral networks
https://arxiv.org/pdf/1312.6199.pdf


## Distilling the knowledge in a Neural Network.
- https://arxiv.org/pdf/1503.02531.pdf
- http://www.ttic.edu/dl/dark14.pdf
- More papers on Distilling - https://github.com/dkozlov/awesome-knowledge-distillation
- Model Compression:
  - transfer the language learned from the ensembled models to a single smaller model to reduce the test computation.
  - Train an ensemble of networks and use their softmax (Use high temperature values to get much softer distribution over the outputs) values (Averaged over ensemble as outputs to train a small network.
  - When distilling use both hard labels and soft-target outputs(above outputs) with relative weight to train the model.
  - Use T = [1, 2, 5, 10] when training both cumbersome models and distill model. For inference on distill model use T=1

- Specialist Networks:
  - When the number of classes are large, Build specialist model on sub-classes which are confusable(Same type of mushroom or dog breeds).
  - While training specilist network, combine all the classes which you don't care into one class (dustbin class)
  - While training specilist networks, half its examples coming from its special subset and half sampled at random from the remainder of the training set. After training, we can correct for the biased training set by incrementing the logit of the dustbin class by the log of the proportion by which the specialist class is oversampled.
