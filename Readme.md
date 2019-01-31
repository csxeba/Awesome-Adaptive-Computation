# Awesome Adaptive Computation
This is an Awesome List of publications about adaptive computation time and conditional computation in 
Artificial Neural Networks.
An Adaptive Computation Neural Network (ACNN) is a network, which can reduce computation time by 
reasoning about its internal state (whether it has finished computation or not).

## Adaptive Computation Time

- [Adaptive Computation Time (ACT)](https://arxiv.org/abs/1603.08983): A base reference paper in this
line of work. Adaptive RNNs, which are able to 'ponder' for more than one iteration on a single timestep. The amount of ponder is regularized to be as small as possible.
- [Spatially Adaptive Computation Time (SACT)](https://arxiv.org/abs/1612.02297): The idea of ACT
applied to the blocks of a ResNet-like architecture. The computation may end before it reaches the
end of the current ResNet block, effectively reducing computation time for easier examples. Spatially
Adaptive Computation Time also employs adaptive computation on the pixel level by leveraging perforated
convolutions (only calculating a subset of the output feature map pixels, and copying the rest from the
previous feature map).
- [SkipNet](https://arxiv.org/abs/1711.09485): simpler form of SACT: the execution of a ResNet block
can simply be skipped entirely, no ACT inside the block.

## Conditional Computation

- [Conditional Computation](https://arxiv.org/abs/1511.06297): the basis paper of this line of
work. This paper aims to drop blocks of computational units in a Neural Network in order to increase
computational speed.
- [IDK Cascade](https://arxiv.org/abs/1706.00885): a cascade of Neural Networks. Each network is able 
to predict its own confidence in generating a final output. If the confidence is low (eg. an "I Don't Know" 
label is predicted), the computation continues with the next Neural Network in the cascade.
- [BranchyNet](https://arxiv.org/abs/1709.01686): similar to the IDK cascade, early exit is possible in
BranchyNet. All output units are executed in training time and in inference time, early exit is done when the
output multinomial distribution's entropy is lower than a predetermined threshold.

