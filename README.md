# Adversarial-Patch-Attacks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1m3j0Bh1ZOKLqn7a1qthpn28Wf8TQdjLI?usp=sharing)

## Replicating this project

**Option 1 (Reccomended):** Click the above "Open In Colab" badge (or upload notebook to Colab) and run in a **GPU** instance. Run All. 

**Option 2:** Upload jupyer notebook to another GPU enabled jupyter environment and run all cells. 

*This project can run on CPU but evaluation will be VERY slow*

## Results

**Results shown for the "car" patch**
| Model     | Transfer Attack | Baseline Error (Top1/Top5)  | Patch Size: 2x2 | Patch Size: 4x4 | Patch Size: 8x8 |
| --------- | --------------- | --------------------------- | --------------- | --------------- | --------------- |
| ResNet34  | No              | (6.67%/0.25%)               | (12.04%/0.70%)  | (19.48%/2.35%)  | (58.01%/10.98%) |
| ResNet18  | Yes             | (6.93%/0.26%)               | (12.05%/0.57%)  | (23.22%/2.21%)  | (39.40%/9.48%)  |
| Vgg16     | Yes             | (6.00%/0.36%)               | (11.79%/1.00%)  | (22.36%/4.31%)  | (37.54%/7.29%)  |


## Model performance without patch attack (ResNet34).  

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Screen%20Shot%202021-12-06%20at%2010.49.00%20PM.png)

## The generated adversarial patches. 

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Screen%20Shot%202021-12-06%20at%2010.49.38%20PM.png)

## Model performance after patch attack (ResNet34). 

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Screen%20Shot%202021-12-06%20at%2010.50.08%20PM.png)

## Transfer Attack - ResNet18

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Screen%20Shot%202021-12-06%20at%2011.06.33%20PM.png)

## Transfer Attack - Vgg16

![alt text](https://github.com/malcolmsfraser/Adversarial-Patch-Attacks/blob/main/images/Screen%20Shot%202021-12-06%20at%2011.07.12%20PM.png)
