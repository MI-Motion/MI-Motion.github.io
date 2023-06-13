# The MI-Motion Dataset and Benchmark for 3D Multi-Person Motion Prediction

## Getting Started


The MI-Motion dataset can be downloaded from [![Google Drive](https://img.shields.io/badge/Google-Drive-blue)](https://drive.google.com/file/d/1HM7pwrT_hxpqgjicAbhCKK45hTvWnC6F/view?usp=sharing) and [![Baidu Disk](https://img.shields.io/badge/Baidu_Disk-PWD:2v41-white)](https://pan.baidu.com/s/1KT0YRxbcqYoyremod-0T7Q). You can also download the pretrained models of all the baselines in [![Google Drive](https://img.shields.io/badge/Google-Drive-blue)](https://drive.google.com/drive/folders/13ZD0BHzADmWzkXs_lxZdbhULLlsIMwkb?usp=sharing). More details could be found in the [Project Page](https://mi-motion.github.io/).
<br/>



## Prepare Dataset
Firstly, you need to unzip the supplementary material and open the project "supp_codes". Then download the dataset and prepare your data like this:
```
your_project_folder/
├── data/
│   ├── MI-Motion
│   │   ├── S0
│   │   ├── S1
│   │   ├── S2
│   │   ├── S3
│   │   ├── S4
│   ├── ├── ...
│   ├── preprocess_data.py
│   ├── ...
├── baselines/
│   ├── ...
├── util/
│   ├── ...

```

## Preprocsess Data
```
cd data
python preprocess_data.py
```


## Training
For any baseline method: 
```
python baselines/train_{method}.py

# example of training for HRI baseline
python baselines/train_hri.py  
```
## Evaluation
For any baseline method: 
```
python baselines/eval_{method}.py
```
If you want evaluation for ultra-long-term prediction, use:
```
python baselines/eval_{method}.py --ultra-long 1
```

## Visualization
```
# for short-term and long term prediction
python baselines/eval_{method}.py --vis 1  

# for ultra-long-term prediction 
python baselines/eval_{method}.py --vis 1 --ultra-long 1 
```
The rendered PNGs and GIFs are automatically saved in output folder of each baseline.



## Acknowledgement
Many thanks to the previous works:
- [HRI](https://github.com/wei-mao-2019/HisRepItself)
- [MRT](https://github.com/jiashunwang/MRT)
- [TBIFormer](https://github.com/xiaogangpeng/TBIFormer) 

Parts of this project page were adopted from the [Nerfies](https://nerfies.github.io/) page.

## Benchmark Codes License
MIT
## Website License
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />
<!-- This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>. -->