# Kaggle_Image_localization


# `Dataset`

source = https://www.kaggle.com/datasets/mbkinaci/image-localization-dataset

---

# Description : 

Including images and its corresponding .xml files. Before drawing bounding boxes, all images were resized to (227,227,3).
3 categories: Cucumber, Eggplant, Mushroom.

![download](https://github.com/Elman295/Kaggle_Image_localization/assets/77393687/1d1de2ea-857e-4ee3-ba4f-b94b49ef0571)

---

# model :

ResNet 18
Total params: 11,243,335
Trainable params: 11,243,335

Input size (MB): 14.05
Forward/backward pass size (MB): 1576.43
Params size (MB): 42.89


---

# Hyperparameter 

Batch size = 16
lr = 1e-3
Droup out p = 0.5 (default)
Epochs = 200

loss function scores = Cross entropy

loss function bounding boxes = MSE (sum of them )

Optimizer = Adam 



---

# result:

dataset sample : 

![download](https://github.com/Elman295/Kaggle_Image_localization/assets/77393687/8438229e-3ea5-4abb-9cbd-b9109ac4748d)

My model result :

![Capture](https://github.com/Elman295/Kaggle_Image_localization/assets/77393687/09cd8fae-5bcc-49e2-bc02-8326015b8042)




