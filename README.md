# Neural-Style-Transfer
Implementing Style Transfer on Images.

This repo provides PyTorch Implementation of MSG-Net and Neural Style transfer for images.

<img src="https://github.com/Ranger105/Neural-Style-Transfer/blob/master/exampl.png">


## Installation
1. Download the pre-trained model

MSG_Net pretrained model download
```
git clone https://github.com/Ranger105/Neural-Style-Transfer.git
cd Neural-Style-Transfer/experiments
bash models/download_model.sh
```
2. Install requirements

  Python packages to run the model.
```
pip install -r requirements.txt
```
3. Camera Demo

  Run model on your webcam.
``` python
python camera_demo.py demo --model models/21styles.model
```

4. Test the model

Run model on varous images stored in folder.
``` 
python main.py eval --content-image images/content/venice-boat.jpg --style-image images/21styles/candy.jpg --model models/21styles.model --content-size 1024
```
  
- ``` --content-image```: path to content image you want to stylize.
- ```--style-image```  : path to style image (typically covered during the training).
- ```--model```        : path to the pre-trained model to be used for stylizing the image.
- ```--output-image``` : path for saving the output image.
- ```--content-size```: the content image size to test on.
