# Program flow

* ResNext-101 model pretrained on kinetics dataset is used to extract features from the video frames (Dataset: tvsum).
* We train an LSTM model attached with a multi-layer perceptron to predict the importance score of each frame.
* Kernel temporal segmentation (KTS) is used to segment the video based on the importance score.
* Average importance of the segments is used as the value in a fractional knapsack problem to select the most important segments.
* moviepy is used to create a summary video from the selected segments.