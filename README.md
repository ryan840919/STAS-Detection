# STAS-Detection
In this project, we join the contest of ['肺腺癌病理切片影像之腫瘤氣道擴散偵測競賽 II：運用影像分割作法於切割STAS輪廓'](https://tbrain.trendmicro.com.tw/Competitions/Details/22), the goal is to use the object detection method to detect the "STAS" of the lung adenocarcinoma. We use ['YOLOv5'](https://github.com/ultralytics/yolov5) model on "colab" enviroment to solve this problem.

## Preprocess
### Color Deconvolution
We first start from some common check on the figures, the [color deconvolution](./Color_Deconvolution_PS.ipynb), there are many ways of doing this, we focus on RGB deconvolution and HistomickTK's deconvolution, but there is no interesting feature after these deconvolution.

### Split the data
We [split the data](./Split_the_data_PS.ipynb) into train set and validation set, which the ratio is about 9:1, notice that we also split the labels.txt files into these sets to match each figures after converting the xml files to txt files.

## Training
We use Yolov5 to [train and validate](./YOLOv5_PS.ipynb) the figures. we also record these results on [Weights & Bias](https://wandb.ai/), which can visulize the training results in a more intuitive way.

## Postprocess
### Prediction and Ground True
We label out the [prediciton and ground true](./Prediction_and_Ground_true.ipynb), which also include the false_positive and false_negative that are defined by IOU, in this way, we can visulize specific the importment part and analyze these area.

### Analysis
We [analyze](./Analysis.ipynb) the false_positive and false_negative area's size and color element, and also devide them by their score.

## Submmision
Last, we [submit](./Submission.ipynb) our train result in a require form back to the contest and get the final test score.
