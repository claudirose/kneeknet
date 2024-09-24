# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 


## Model Description


**Input:** 
A 162x300 x-ray image of a single human knee joint.


**Output:** 
The grade of osteoarthritis according to the Kellgren and Lawrence grading system:
- G0 (Normal)
- G1 (Doubtful)
- G2 (Mild)
- G3 (Moderate)
 -G4 (Severe)


**Model Architecture:** 
The CNN uses the LeNet architecture. It consists of two convolution layers, two max pooling layers and three fully connected layers.
- The convolution kernel has size (5x5), a stride of 1 and no padding.
- The max pooing kernel has size (2x2), a stride of 2 and no padding.
- The first fully connected layer has 120 output features (neurons)
- The second fully connected layer has 84 output features (neurons)
- The ReLu activation function is applied after each convolution and fully connected layer.

The optimiser used is toch.optim.Adam and the criterion used is torch.nn.CrossEntropyLoss.

## Performance

The model is trained on a random 75% sample of the single-knee image data, and tested on the remaining 25%. An accuracy of 60% is achieved on the unseen test data. 

The accuracy per class is as follows:
- G0
- G1
- G2
- G3
- G4

The confusion matrix for performance on the test data can be seen below.

## Limitations

Outline the limitations of your model.

## Trade-offs

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 
