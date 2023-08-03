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

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1         [16, 64, 139, 139]           9,408
       BatchNorm2d-2         [16, 64, 139, 139]             128
              ReLU-3         [16, 64, 139, 139]               0
         MaxPool2d-4           [16, 64, 70, 70]               0
            Conv2d-5           [16, 64, 70, 70]          36,864
       BatchNorm2d-6           [16, 64, 70, 70]             128
              ReLU-7           [16, 64, 70, 70]               0
            Conv2d-8           [16, 64, 70, 70]          36,864
       BatchNorm2d-9           [16, 64, 70, 70]             128
             ReLU-10           [16, 64, 70, 70]               0
       BasicBlock-11           [16, 64, 70, 70]               0
           Conv2d-12           [16, 64, 70, 70]          36,864
      BatchNorm2d-13           [16, 64, 70, 70]             128
             ReLU-14           [16, 64, 70, 70]               0
           Conv2d-15           [16, 64, 70, 70]          36,864
      BatchNorm2d-16           [16, 64, 70, 70]             128
             ReLU-17           [16, 64, 70, 70]               0
       BasicBlock-18           [16, 64, 70, 70]               0
           Conv2d-19          [16, 128, 35, 35]          73,728
      BatchNorm2d-20          [16, 128, 35, 35]             256
             ReLU-21          [16, 128, 35, 35]               0
           Conv2d-22          [16, 128, 35, 35]         147,456
      BatchNorm2d-23          [16, 128, 35, 35]             256
           Conv2d-24          [16, 128, 35, 35]           8,192
      BatchNorm2d-25          [16, 128, 35, 35]             256
             ReLU-26          [16, 128, 35, 35]               0
       BasicBlock-27          [16, 128, 35, 35]               0
           Conv2d-28          [16, 128, 35, 35]         147,456
      BatchNorm2d-29          [16, 128, 35, 35]             256
             ReLU-30          [16, 128, 35, 35]               0
           Conv2d-31          [16, 128, 35, 35]         147,456
      BatchNorm2d-32          [16, 128, 35, 35]             256
             ReLU-33          [16, 128, 35, 35]               0
       BasicBlock-34          [16, 128, 35, 35]               0
           Conv2d-35          [16, 256, 18, 18]         294,912
      BatchNorm2d-36          [16, 256, 18, 18]             512
             ReLU-37          [16, 256, 18, 18]               0
           Conv2d-38          [16, 256, 18, 18]         589,824
      BatchNorm2d-39          [16, 256, 18, 18]             512
           Conv2d-40          [16, 256, 18, 18]          32,768
      BatchNorm2d-41          [16, 256, 18, 18]             512
             ReLU-42          [16, 256, 18, 18]               0
       BasicBlock-43          [16, 256, 18, 18]               0
           Conv2d-44          [16, 256, 18, 18]         589,824
      BatchNorm2d-45          [16, 256, 18, 18]             512
             ReLU-46          [16, 256, 18, 18]               0
           Conv2d-47          [16, 256, 18, 18]         589,824
      BatchNorm2d-48          [16, 256, 18, 18]             512
             ReLU-49          [16, 256, 18, 18]               0
       BasicBlock-50          [16, 256, 18, 18]               0
           Conv2d-51            [16, 512, 9, 9]       1,179,648
      BatchNorm2d-52            [16, 512, 9, 9]           1,024
             ReLU-53            [16, 512, 9, 9]               0
           Conv2d-54            [16, 512, 9, 9]       2,359,296
      BatchNorm2d-55            [16, 512, 9, 9]           1,024
           Conv2d-56            [16, 512, 9, 9]         131,072
      BatchNorm2d-57            [16, 512, 9, 9]           1,024
             ReLU-58            [16, 512, 9, 9]               0
       BasicBlock-59            [16, 512, 9, 9]               0
           Conv2d-60            [16, 512, 9, 9]       2,359,296
      BatchNorm2d-61            [16, 512, 9, 9]           1,024
             ReLU-62            [16, 512, 9, 9]               0
           Conv2d-63            [16, 512, 9, 9]       2,359,296
      BatchNorm2d-64            [16, 512, 9, 9]           1,024
             ReLU-65            [16, 512, 9, 9]               0
       BasicBlock-66            [16, 512, 9, 9]               0
AdaptiveAvgPool2d-67            [16, 512, 1, 1]               0
           Linear-68                  [16, 128]          65,664
      BatchNorm1d-69                  [16, 128]             256
             ReLU-70                  [16, 128]               0
           ResNet-71                  [16, 128]               0
           Linear-72                    [16, 3]             387
           Linear-73                    [16, 4]             516
================================================================
Total params: 11,243,335
Trainable params: 11,243,335
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 14.05
Forward/backward pass size (MB): 1576.43
Params size (MB): 42.89
Estimated Total Size (MB): 1633.37
----------------------------------------------------------------

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




