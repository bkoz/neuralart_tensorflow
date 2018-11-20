## NeuralArt

Implementation of [A Neural Algorithm of Artistic Style](http://arxiv.org/abs/1508.06576) by Tensorflow.

### Requirements
 - [Tensorflow](http://www.tensorflow.org/)
 - [VGG 19 model](https://drive.google.com/file/d/0B8QJdgMvQDrVU2cyZjFKU1RrLUU/view?usp=sharing)

### OpenShift Demo
 - Create the TensorFlow pod
   - oc create -f tensorflow.yaml
   - oc expose service tensorflow
 - Download the [VGG 19 model](http://presto.eadgbe.net/bkozdemb/data/imagenet-vgg-verydeep-19.mat)
 - Copy the Jupyter notebook directory to the running pod.
   - oc rsync neuralart_tensorflow tensorflow:/notebooks
 - Obtain the route and token to visit the notebook.
   - oc logs tensorflow
   - oc get routes tensorflow
 - Visit the Jupyter Notebook and run the neuralart_tensorflow notebook.ipynb

### Examples

<p>
Content: <br/>
<img src="https://github.com/ckmarkoh/neuralart_tensorflow/blob/master/images/Taipei101.jpg?raw=true" width="50%"/> <br/>
Style: <br/>
<img src="https://github.com/ckmarkoh/neuralart_tensorflow/blob/master/images/StarryNight.jpg?raw=true" width="50%"/> <br/>
Output: <br/>
<img src="https://github.com/ckmarkoh/neuralart_tensorflow/blob/master/images/Taipei101_StarryNight.jpg?raw=true" width="50%"/> <br/>
</p>
