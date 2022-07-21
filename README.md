# STAS-Detection
In this project, we join the contest of ['肺腺癌病理切片影像之腫瘤氣道擴散偵測競賽 II：運用影像分割作法於切割STAS輪廓'](https://tbrain.trendmicro.com.tw/Competitions/Details/22), the goal is to use the object detection method to detect the "STAS" of the lung adenocarcinoma. We use ['YOLOv5'](https://github.com/ultralytics/yolov5) model on "colab" enviroment to solve this problem.

## Preprocess
We first start from some common check on the figures, the [color deconvolution](./Color_Deconvolution_PS.ipynb), there are many ways of doing this, we focus on RGB deconvolution and HistomickTK's deconvolution, but there is no interesting feature after these deconvolution.
