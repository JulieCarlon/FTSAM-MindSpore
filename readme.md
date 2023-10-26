# Enhancing Fine-Tuning based Backdoor Defense with Sharpness-Aware Minimization

This is the official MindSpore implementation of [Enhancing Fine-Tuning based Backdoor Defense with Sharpness-Aware Minimization](https://openaccess.thecvf.com/content/ICCV2023/papers/Zhu_Enhancing_Fine-Tuning_Based_Backdoor_Defense_with_Sharpness-Aware_Minimization_ICCV_2023_paper.pdf)

## Requirements
see file `mindspore.yaml`

## Datasets and state-of-the-art backdoor attack and defense methods.
We test our method on CIFAR-10, Tiny ImageNet and GTSRB datasets.
For CIFAR-10, the dataset will be download automatically. We follow [BackdoorBench](https://github.com/SCLBD/BackdoorBench) on the implementation of SOTA attack and defense methods.

## Running the code
Before run the defense method, a backdoored model should be generated first. We provide the script for defense on CIFAR-10 dataset.

### Step 1 Prepare a poisoned dataset.
    python attack/data_poison.py
### Step 2 Train a backdoored model
    python attack/train_backdoor.py

### Step 3 Run the defense
    python defense/ft_sam.py

If you use this paper/code in your research, please consider citing us:

```
@InProceedings{Zhu_2023_ICCV,
    author    = {Zhu, Mingli and Wei, Shaokui and Shen, Li and Fan, Yanbo and Wu, Baoyuan},
    title     = {Enhancing Fine-Tuning Based Backdoor Defense with Sharpness-Aware Minimization},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2023},
    pages     = {4466-4477}
}
```

## Acknowledgment
Our project references the codes in the following repos.
- [BackdoorBench](https://github.com/SCLBD/BackdoorBench)
- [SAM](https://github.com/davda54/sam)