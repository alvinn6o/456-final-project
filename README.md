MobileNetV2 Base Model Transfer Learning CNN Project

The notebook "mobile.ipynb" has the transfer learning example with a base model MobileNetV2

Dataset is in the directory data/ with 10 classes
- 26179 files total
80-20 split
- 20944 training file examples
- 5235 validation file examples


Model Architecture
- Base model: MobileNetV2 which is light weight (compared to other models such as ResNet50) with much less parameters, but still good
- Transfer learning head
    - Applied global average pooling to keep parameters low and model lighter weight
    - Dropout of 30% neurons
    - Then 10 neurons in the final layer to match class numbers (softmax)


Data augmentation
- Applied class concepts of augmentation (flip and rotation and zoom) to prevent memorization and overfitting


Data Normalization
- Normalized to [-1, 1] which is standard for MobileNet according to documentation


To run the notebook please ensure you have all libraries installed in requirements.