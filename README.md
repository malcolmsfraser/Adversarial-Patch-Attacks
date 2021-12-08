# Adversarial-Patch-Attacks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1m3j0Bh1ZOKLqn7a1qthpn28Wf8TQdjLI?usp=sharing)

## Replicating this project

**Option 1 (Reccomended):** Click the above "Open In Colab" badge (or upload notebook to Colab) and run in a **GPU** instance. Run All. 

**Option 2:** Upload jupyer notebook to another GPU enabled jupyter environment and run all cells. 

*This project can run on CPU but evaluation will be VERY slow*

## Results

**Results shown for the "car" patch**

### Top1 and Top5 Error
| Model     | Transfer Attack | Baseline Error  | Patch Size: 2x2 | Patch Size: 4x4 | Patch Size: 8x8 | Patch Size: 16x16 |
| --------- | --------------- | --------------- | --------------- | --------------- | --------------- | ----------------- |
| ResNet34  | No              | (6.67%/0.25%)   | (12.04%/0.70%)  | (19.48%/2.35%)  | (58.01%/10.98%) | (89.90%/40.17%)   |
| ResNet18  | Yes             | (6.93%/0.26%)   | (12.05%/0.57%)  | (23.22%/2.21%)  | (39.40%/9.48%)  | (87.77%/30.96%)   |
| Vgg16     | Yes             | (6.00%/0.36%)   | (11.79%/1.00%)  | (22.36%/4.31%)  | (37.54%/7.29%)  | (83.34%/34.60%)    |

### Top1 and Top5 Patch Accuracy
| Model     | Transfer Attack | Patch Size: 2x2 | Patch Size: 4x4 | Patch Size: 8x8 | Patch Size: 16x16 |
| --------- | --------------- | --------------- | --------------- | --------------- | ----------------- |
| ResNet34  | No              | (0.99%/19.27%)  | (5.14%/47.34%)  | (83.73%/98.85%) | (99.99%/100%)     |
| ResNet18  | Yes             | (0.89%/24.11%)  | (10.04%/66.90%) | (59.69%/92.75%) | (99.15%/100%)     |
| Vgg16     | Yes             | (0.88%/31.89%)  | (5.70%/50.08%)  | (10.98%/35.75%) | (96.11%/99.72%)   |


## The generated adversarial patches. 

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Patches-300dpi.png)

## Model performance after patch attack (ResNet34). 

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet34_dog_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet34_truck_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet34_ship_w_catPatch8_300dpi.png)

## Transfer Attack - ResNet18

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet18_dog_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet18_truck_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/resnet18_ship_w_catPatch8_300dpi.png)

## Transfer Attack - Vgg16

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/vgg16_dog_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/vgg16_truck_w_catPatch8_300dpi.png)
![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/vgg16_ship_w_catPatch8_300dpi.png)
