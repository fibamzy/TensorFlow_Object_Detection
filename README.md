# Tensorflow Object Detection Walkthrough
<p>The notebooks in this repository are tailored towards developing custom object detection models using TensorFlow.

<p>Stepwise guideline is itemized below.<br> 

<img width="150" height="100" src="https://github.com/fibamzy/TensorFlow_Object_Detection/blob/main/output_samples/OK.png?raw=true">
<img width="150" height="100" src="https://github.com/fibamzy/TensorFlow_Object_Detection/blob/main/output_samples/NOK.png?raw=true">

## Steps
<br />
<b>Step 1.</b> Clone this repository
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv tfod
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfod
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://github.com/fibamzy/TensorFlow_Object_Detection/blob/main/1.%20Image%20Collection.ipynb">1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TFODCourse\Tensorflow\workspace\images\train<br />
\TFODCourse\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Train your model using <a href="https://github.com/fibamzy/TensorFlow_Object_Detection/blob/main/2.%20Training%20and%20Detection.ipynb">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<img src="https://i.imgur.com/FSQFo16.png">
If not, resolve installation errors by referring to the <a href="https://github.com/fibamzy/TensorFlow_Object_Detection/blob/main/Error%20Guide.md">Error Guide.md</a> in this folder.
<br /> <br/>
<b>Step 9.</b> Train the model at step 6, from within the notebook or in a separate terminal if you want to display live loss metrics. 
<img src="https://i.imgur.com/K0wLO57.png"> 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorflow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. <br>
OR for the training module "..\tfod\TFODCourse\Tensorflow\workspace\models\my_ssd_mobnet_5\train>tensorboard --logdir=."</pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
