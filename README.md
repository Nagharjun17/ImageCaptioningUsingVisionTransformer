# Image_Captioning_Using_Vision_Transformer

Our project aims to address the critical challenge of generating descriptive sentences from images, which lies at the intersection of computer vision and natural language processing. With over 12 million visually impaired individuals [1] above the age of 40 in the United States alone, our proposed solution has the potential to enhance accessibility. Our approach involves training a transformer-based deep learning model, to understand the image and generate linguistically accurate captions. The encoder part utilizes a pre-trained Vision Transformer to extract features from an image. After extracting the features, they are fed to the transformer decoder network to generate captions. We evaluated our model's performance using standard evaluation metrics such as BLEU on the Flickr8K dataset. The Vision Transformer model was able to extract features on par and higher against other traditional CNN architectures in terms of quality. Our approach has potential applications in enabling more efficient image retrieval systems and improving accessibility for visually impaired individuals.

## Dataset:
The Flickr8K dataset is a widely used benchmark for sentence-based image description. It comprises 8092 images in JPEG format with varying shapes and sizes, of which 6000 are used for training, 1000 for testing, and 1000 for development. The Flickr8K text folder contains text files that describe the train set and test set, while the Flickr8K.token.txt file contains five captions for each image, totaling 40460 captions. The dataset has become a standard benchmark for beginners in the field of sentence-based image description and has been used in various deep learning projects, including image caption generators that use CNN and LSTM units to recognize the context of an image and describe it in natural language. The Flickr8K dataset has also been used in studies exploring the possibility of textual and visual modalities sharing a common embedding space.

## Model Architecture:

![TransformerNetwork](https://github.com/Nagharjun17/Image_Captioning_Using_Vision_Transformer/assets/64778259/61e5f228-35ed-40c8-93dd-da0ffef3b17f)



## Usage
The `VisionCaption.ipynb` file can run locally through Jupyter Notebook or Google Colab.

Before running, go to the mentioned link below and download the glove.6B.100d.txt.zip which contains the word embeddings. 
Link: https://drive.google.com/file/d/12OE-X3innao-uHeMbZqe_lG19iFkEhSX/view?usp=sharing

If you are using google colab, just upload the .zip file to the instance. 

Requirements:

Run the below command in the terminal to install dependencies.

`pip install -r requirements.txt`


## Performance and Results:

Vision Transformer as the Encoder:
 |Epochs| 1-gram BLEU |2-gram BLEU|3-gram BLEU|4-gram BLEU|
 |-------|------|-------|-----|----|
| 10   | 42.177    |25.6924|   14.33078|7.1955|
 |20|   58.279  | 39.3787   |24.7216|14.5401|
 |30 |67.186 | 47.0968|  31.0677|19.6122|
 |40|69.532 | 49.6889|  33.4294|21.5386|

 |Encoder| 1-gram BLEU |2-gram BLEU|3-gram BLEU|4-gram BLEU|
|---|---|---|---|---|
 |ViT   |67.186 | 47.0968|  31.0677|19.6122|
 |ResNet50|   65.765  | 45.423  |29.892|18.236|
 |Inception |63.825 | 44.055|  28.74|17.813|
 |DenseNet|61.758 | 42.0103|  26.814|16.268|

|Parameters|Values|
|----|-----|
 |Loss Function | Cross Entropy|
 |Learning Rate | 0.00001|
 |Batch Size | 32|
 |Optimizer | Adam|
 |Regularization | L2 Penalty|
 |Gradient Regularization | Gradient Clipping|
 
 
 <img width="509" alt="Screen Shot 2023-05-16 at 5 55 41 PM" src="https://github.com/Nagharjun17/Image_Captioning_Using_Vision_Transformer/assets/64778259/3ab7d987-59bd-4787-94ce-1ffa788b25f8">

 <img width="512" alt="Screen Shot 2023-05-16 at 5 56 12 PM" src="https://github.com/Nagharjun17/Image_Captioning_Using_Vision_Transformer/assets/64778259/b990627d-533e-4449-8f09-4498b50f134d">
 
 

 
