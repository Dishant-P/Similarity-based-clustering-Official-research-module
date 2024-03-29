# Similarity-based clustering for enhancing Image classification architectures

There are three parts to this code.
1. Feature extraction
2. Cluster formations
3. Model trainings (VGG-19, VGG-16, ResNet50, ResNeXt50, AlexNet)

## Code usage

### Folder management for feature extraction
You need to add your images into a directory called __database/__, so it will look like this:

    ├── src/            # Source files
    ├── cache/          # Generated on runtime for feature extraction file
    ├── models/         # Containing all the model training files
    ├── README.md       # Intro to the repo
    └── database/       # Directory of all your images

__all your images should be put into database/__

In this directory, each image class should have its own directory and the images belonging to that class should put into that directory.

To get started with feature extraction, run the feature extraction code through ```python resnet.py``` after following the env steps and folder management as described there. 
Once you run the above code, visit the cache/ directory where you will find hte extracted features file. The same file will be used in the next step.

### Cluster formations
The cluster formation script can be run simply by the following code:
```python Cluster formation.py```
Note: Make sure to edit the path to the extracted features file and the dataset folder before running the above command.

### Model trainings

The model trainings are straightforward. The only thing to change is the initials path values for your dataset splits. You can access all six versions of all three datasets on this [link](https://bit.ly/SBC-ICA-dataset-splits) as well. 

## Results of training and computational resource usage(s).

### Validation accuracies with each cluster split per epoch.
<img src="/images/Val-sbcica-1.png" width="700">

### Computational resources used for each cluster split for same dataset.
<img src="/images/resources-sbcica-1.png" width="600">

## Credits

Original dataset credits are to their respective authors:
1. A. Khosla, N. Jayadevaprakash, B. Yao, F.-F. Li, Novel dataset for fine-grained image categorization: Stanford dogs, in: Proc. CVPR Workshop
on Fine-Grained Visual Categorization (FGVC), Vol. 2, 2011.
2. Nilsback, Maria-Elena, and Andrew Zisserman. "Automated flower classification over a large number of classes." 2008 Sixth Indian Conference on Computer Vision, Graphics & Image Processing. IEEE, 2008.

Feature extraction is based on the work of Po-Chih Huang's CBIR system based on ResNet features.

If you want to cite the entire work of Similarity-based clustering for enhancing Image classification architectures please make sure to include the full citiation as follows:

>@article{parikh2021similarity,  
>  title={Similarity-Based Clustering for Enhancing Image Classification Architectures},  
>  author={Parikh, Dishant},  
>  journal={arXiv preprint arXiv:2011.04728},  
>  year={2021}  
>}  

## Author
Dishant Parikh | [DishantP](https://github.com/Dishant-P)
