<h2>TensorFlow-FlexUNet-Image-Segmentation-EMIDEC (2026/07/19)</h2>
Sarah T.  Arai<br>
Software Laboratory antillia.com<br><br>
This is the second experiment of Image Segmentation for 
<a href="https://emidec.com/dataset"><b>
EMIDEC (Evaluation of Myocardial Infarction from Delayed-Enhancement Cardiac MRI)
</b>
</a> based on our <a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
TensorFlow-FlexUNet-Image-Segmentation-Model</a> 
(TensorFlow Flexible UNet Image Segmentation Model for Multiclass) , 
and a 512x512 pixels PNG
<a href="https://drive.google.com/file/d/17P8uRqDm4flK6sXtcm7rY2XU7ciESE2Y/view?usp=sharing">
<b>EMIDEC-Heart-MRI-ImageMask-Dataset-V2.zip</b></a> with colorized masks 
(<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode">CC BY-NC-SA 4.0</a>), which was derived by us from <br><br>
<a href="https://www.kaggle.com/datasets/johnsonhk88/emidec-dataset-for-heart-mri-image">
<b>EMIDEC Dataset For Heart MRI Image</b> </a> by ohnson chong.
<br><br>
<hr>
<b>Actual Image Segmentation for EMIDEC-Heart-MRI of 512x512 pixels </b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the 
ground truth masks, except the third case.
<br><br>
<b>class_color_map={class_1:blue, class_2:green, class_3:red, class_4:cyan}</b>
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/10001_7.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/10001_7.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/10001_7.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/deformed_alpha_1300_sigmoid_9_10055_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/deformed_alpha_1300_sigmoid_9_10055_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/deformed_alpha_1300_sigmoid_9_10055_5.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/distorted_0.01_rsigma0.5_sigma40_10042_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/distorted_0.01_rsigma0.5_sigma40_10042_5.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/distorted_0.01_rsigma0.5_sigma40_10042_5.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1  Dataset Citation</h3>
The dataset used here was derived from <br><br>
<a href="https://www.kaggle.com/datasets/johnsonhk88/emidec-dataset-for-heart-mri-image">
<b>EMIDEC Dataset For Heart MRI Image</b> </a> by ohnson chong.<br><br>
The following explanation was taken from the web site.
<br><br>
<b>About Dataset</b><br>
<b>Dataset Information</b><br>
EMIDEC (Evaluation of Myocardial Infarction from Delayed-Enhancement Cardiac MRI) is a dataset aimed at 
assessing the extent of myocardial infarction. <br>
This dataset includes delayed-enhancement magnetic resonance imaging (DE-MRI) of multiple patients 
taken minutes after contrast injection, manually annotated to identify several myocardial 
infarction-related areas including the myocardial outline, infarction regions, 
and permanent microvascular obstruction areas (no reflow zones), forming a segmentation dataset. <br>
It comprises 150 cases (all from different patients), including 50 cases with normal MRI
 post-contrast injection and 100 cases of myocardial infarction (appearing as enhanced areas on DE-MRI).<br>
The dataset includes 100 training cases and 50 test cases.
<br><br>
The dataset, with 150 clinical MRI images and associated clinical features of myocardial infarction, 
holds significant research value. <br>
It provides a foundation for assessing and automatically detecting myocardial infarctions, aiding in 
the development of automated algorithms to identify areas of myocardial damage, and supporting 
the development of diagnostic tools based on imaging and clinical data. <br>
Due to its large number of cases and comprehensive information, 
this dataset has significant potential for application in the diagnosis and treatment of myocardial infarction.
<br><br>
<b>Dataset Meta Information</b><br>
Dimensions Modality Task Type Anatomical Area Number of Categories Data Volume File Format
3D DE-MRI Segmentation Heart 4 150 .nii.gz<br><br>
<b>Resolution Details</b><br>
Dataset Statistics spacing (mm) size<br>
min (1.367, 1.367, 8.0) (139, 120, 4)<br>
median (1.458, 1.458, 10.0) (240, 256, 7)<br>
max (1.875, 1.875, 13.04) (305, 308, 10)<br>
<br>
Number of 2D slices in the dataset: 708.<br>
<br>
<b>Label Information Statistics</b><br>
Only 100 examples in the training set are counted.<br><br>
<table border="1">
<tr>
<th>Region</th>
<th> Number of Cases</th>
<th>Completion Rate</th>
<th> Minimum Volume (cm³)</th>
<th> Median Volume (cm³)</th>
<th> Maximum Volume (cm³)</th>
</tr>
<tr>
<td>Left Ventricle</td><td>100</td><td>100%</td><td> 49.28</td><td>105.46</td><td> 280.77</td>
</tr>
<tr>
<td>Myocardium</td><td>100</td><td>100%</td><td> 53.81</td><td> 96.5</td><td> 153.83</td>
</tr>
<tr>
<td>Myocardial Infarction</td><td> 67</td><td> 67%</td><td> 2.39</td><td> 20.26</td><td> 80.1</td>
</tr>
<tr>
<td>No Reflow</td><td> 40</td><td> 40%</td><td> 0.32</td><td> 2.35</td><td> 36.74</td>
</tr>
</table>

<br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode">CC BY-NC-SA 4.0</a>
<br><br>
For more information, please refer to <a href="https://emidec.com/dataset"><b>MIDEC the database</b>
></a>
<br><br>
<h3>
2 EMIDEC-Heart-MRI ImageMask Dataset
</h3>
<h3>
2.1 Download ImageMask Dataset
</h3>
 If you would like to train this EMIDEC-Heart-MRI Segmentation model by yourself,
please down load our dataset <a href="https://drive.google.com/file/d/17P8uRqDm4flK6sXtcm7rY2XU7ciESE2Y/view?usp=sharing">
<b>EMIDEC-Heart-MRI-ImageMask-Dataset-V2.zip</b>
(<a href="https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode">CC BY-NC-SA 4.0</a>)
</a> on the google drive,
expand the downloaded, and put it under <b>./dataset/</b> to be.
<pre>
./dataset
└─EMIDEC-Heart-MRI
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
        ├─images
        └─masks
</pre>
<br>
<b>EMIDEC-Heart-MRI Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/EMIDEC-Heart-MRI_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is large enough to use for a training set of our segmentation model.
<br><br>
<h3>
2.2 Derivation of EMIDEC-Heart-MRI-ImageMask Dataset
</h3>
The folder structure of the original <b>emidec_dataset</b> is the following.
<pre>
./emidec-dataset-1.0.1
├─Case_N006
│  ├─Contours
│  │  └─Case_N006.nii
│  └─Images
│      └─Case_N006.nii
...
└─Case_P100
    ├─Contours
    │  └─Case_P100.nii
    └─Images
        └─Case_P100.nii
</pre>
<b>Step 1</b><br>
We generated a 512x512 pixsels cropped PNG ImageMask Dataset with colorized masks from the NIfTI files in 
all
<b>Contours</b> and <b>Images</b> folders, by using the follwing <b>class(pixel value of contour mask)</b> and 
<b>color_mapping table</b>.<br><br>
<b>class_color_map={1:blue, 2:green, 3:red, 4:cyan}</b>
<br><br> 
<b>Step 2</b><br>
We finally generated our own <a href="https://drive.google.com/file/d/17P8uRqDm4flK6sXtcm7rY2XU7ciESE2Y/view?usp=sharing"><b>Augmented-EMIDEC-Heart-MRI-ImageMask-Dataset-V2</b></a>
from the PNG ImageMask Dataset 
by using the following offline image augmentation tools.<br>
<a href="https://github.com/sarah-antillia/Image-Deformation-Tool">Image-Deformation-Tool</a><br>
<a href="https://github.com/sarah-antillia/Image-Distortion-Tool">Image-Distortion-Tool</a><br>
<br>
<h3>
2.3 Train Sample Images and Masks
</h3>
<b>Train_sample images</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_sample_masks</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/train_masks_sample.png" width="1024" height="auto">
<br>
<h3>
3 Train TensorflowFlexUNet Model
</h3>
 We trained EMIDEC-Heart-MRI TensorflowFlexUNet Model by using the following
<a href="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters=16</b> and a large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a <b>large num_layers=8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 5
base_filters   = 16
base_kernels  = (11,11)
num_layers    = 8
dropout_rate   = 0.05
dilation       = (1,1)
</pre>

<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>

<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and "dice_coef_multiclass".<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b >Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b></b><br>
<b>RGB color map</b><br>
rgb color map dict for EMIDEC-Heart-MRI 1+4 classes.<br>
<pre>
[mask]
mask_file_format = ".png"
mask_file_format = ".png"
; EMIDEC-Heart-MRI 1+4
;   Background;black,  class1:blue. class2:green, class3:red class4:cyan
rgb_map = {(0, 0, 0):0,(0,0,255):1, (0,255,0):2,(255, 0, 0):3, (0,255,255):4}
</pre>
<b>Epoch change inference callbacks</b><br>
Enabled epoch_change_infer callback.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
epoch_changeinfer        = False
epoch_changeinfer_dir    = "./epoch_changeinfer"
num_infer_images         = 6
</pre>
By using this epoch_change_infer callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> <br> 
<b>Epoch_change_inference output at starting (1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middle-point (28,29,30)</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/epoch_change_infer_at_middlepoint.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (58,59,60)</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>

<br>
In this experiment, the training process was stopped at epoch 25 by EarlyStoppingCallback.<br><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/train_console_output_at_epoch60.png" width="880" height="auto"><br>
<br>
<a href="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI</b> folder,<br>
and run the following bat file to evaluate TensorflowFlexUNet model for EMIDEC-Heart-MRI.<br>
<pre>
>./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetEvaluator.py  ./train_eval_infer.config
</pre>
Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/evaluate_console_output_at_epoch60.png" width="880" height="auto">
<br><br>Image-Segmentation-EMIDEC-Heart-MRI

<a href="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this EMIDEC-Heart-MRI/test was low, and dice_coef_multiclass high as shown below.
<br>
<pre>
categorical_crossentropy,0.0141
dice_coef_multiclass,0.9931
</pre>
<br>
<h3>5 Inference</h3>
Please move to <b>./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI</b> folder<br>
,and run the following bat file to infer segmentation regions for images by the Trained-TensorflowFlexUNet model for EMIDEC-Heart-MRI.<br>
<pre>
>./3.infer.bat
</pre>
This simply runs the following command.
<pre>
>python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/mini_test_masks.png" width="1024" height="auto"><br>
<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks for  EMIDEC-Heart-MRI of 512x512 pixels</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the 
ground truth masks, except the fourth and sixth cases.In these cases,this model failed to detect the class_4 cyan regions.
<br><br>
<b>class_color_map={class_1:blue, class_2:green, class_3:red, class_4:cyan}</b>
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/10001_0.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/10001_0.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/10001_0.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/10046_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/10046_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/10046_2.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/deformed_alpha_1300_sigmoid_8_10055_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/deformed_alpha_1300_sigmoid_8_10055_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/deformed_alpha_1300_sigmoid_8_10055_3.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/deformed_alpha_1300_sigmoid_9_10053_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/deformed_alpha_1300_sigmoid_9_10053_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/deformed_alpha_1300_sigmoid_9_10053_3.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/distorted_0.01_rsigma0.5_sigma40_10037_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/distorted_0.01_rsigma0.5_sigma40_10037_3.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/distorted_0.01_rsigma0.5_sigma40_10037_3.png" width="320" height="auto"></td>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/images/distorted_0.01_rsigma0.5_sigma40_10067_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test/masks/distorted_0.01_rsigma0.5_sigma40_10067_2.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/EMIDEC-Heart-MRI/mini_test_output/distorted_0.01_rsigma0.5_sigma40_10067_2.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. Contrast-Free Myocardial Infarction Segmentation with Attention U-Net</b><br>
Khaled Ali Deeb, Yasmeen Alshelle, Hala Hammoud, Andrey Briko, Vladislava Kapravchuk,<br>
 Alexey Tikhomirov, Amaliya Latypova, Ahmad Hammoud<br>
<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12984793/">
https://pmc.ncbi.nlm.nih.gov/articles/PMC12984793/
</a>
<br>
<br>
<b>2. EMIDEC the database</b><br>
<a href="https://emidec.com/dataset">https://emidec.com/dataset</a>
<br>
<br>
<b>3. Cardiac Atlas Project</b><br>
<a href="https://www.cardiacatlas.org/">https://www.cardiacatlas.org/</a>
<br>
<br>
<b>4. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai <br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br>
<br>
