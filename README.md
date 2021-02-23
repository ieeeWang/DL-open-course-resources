--------------------------------------------------------------------------------

# Useful ML/DL open-course resources

**My personal path** to learn Deep Learning. 


## Table of Contents
<ul>
<li><a href="#Open-course">Open course</a></li>
<li><a href="#GitHub-tutorial-projects">GitHub tutorial projects</a></li>
<li><a href="#Blogs-and-manuals">Blogs and manuals</a></li>
<li><a href="#Books">Books</a></li>
<li><a href="#Common-issues">Common issues</a></li>
</ul>

## Open course
**ranking by popularity**

| No.   | Open course                                            |Tool       | Links           |
| :----:| :----:                                              | :----:   | :----:          |
| 1     | Machine Learning by Andrew Ng  | -  | [coursera](https://www.coursera.org/learn/machine-learning)|
| 2     | Introduction to Deep Learning by MIT  |  tf2.x, Colab | [website](http://introtodeeplearning.com/), [YouTube](https://www.youtube.com/playlist?list=PLtBw6njQRU-rwp5__7C0oIVt26ZgjG9NI)|
| 3     | Deep Learning Specialization by Andrew Ng  | tf1.x, tf2.x |  [coursera](https://www.coursera.org/specializations/deep-learning), [网易](https://mooc.study.163.com/smartSpec/detail/1001319001.htm/)|
| 4     | Convolutional Neural Networks for Visual Recognition by F. Li (Stanford)  | PyTorch, tf2.x | [website](http://cs231n.stanford.edu/)|
| 5     | Natural Language Processing with Deep Learning by C. Manning (Stanford)  |  PyTorch  | [website](http://web.stanford.edu/class/cs224n/), [YouTube](https://www.youtube.com/playlist?list=PLoROMvodv4rOhcuXMZkNm7j3fVwBBY42z)|
| 6     | Deep Learning by Yann LeCun (NYU)  | PyTorch  | [website](https://atcold.github.io/pytorch-Deep-Learning/), [YouTube](https://www.youtube.com/playlist?list=PLLHTzKZzVU9eaEyErdV26ikyolxOsz6mq)|
| 7     | Practical Deep Learning for Coders by Jeremy Howard  | PyTorch, fastai  | [website](https://course.fast.ai/)|
| 8     | 3bule1brown | - |[YouTube](https://www.youtube.com/watch?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&v=aircAruvnKk&feature=youtu.be), [B站](https://space.bilibili.com/88461692/#/) |


## GitHub tutorial projects

| No.   | Project                                  | Remark           |
| :----:| :----:                                   | :----:          |
| 1   | [A Whirlwind Tour of Python](https://github.com/jakevdp/WhirlwindTourOfPython)    | python beginner |
| 2   | [Machine Learning with TensorFlow](https://github.com/BinRoot/TensorFlow-Book)    | good |
| 3   | [30天吃掉那只TensorFlow2](https://github.com/lyhue1991/eat_tensorflow2_in_30_days)   | great|
| 4   | [20天吃掉那只Pytorch](https://github.com/lyhue1991/eat_pytorch_in_20_days)    | great|
| 5   | [Probabilistic Programming and Bayesian Methods for Hackers](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers)    | Probabilistic programming, pyMC3|

## Blogs and manuals
| No.   | books and blogs                          | Remark           |
| :----:| :----:                                   | :----:          |
| 1   | [NumPy for MATLAB users](https://numpy.org/doc/stable/user/numpy-for-matlab-users.html)   | 10 mins |
| 2   | [Python Numpy Tutorial](https://cs231n.github.io/python-numpy-tutorial/#arrays)    | 10 mins|
| 3   | [刘江的python blog](https://www.liujiangblog.com/course/python/3) | 简洁中文指南|
| 4   | [Chriss Olah’s blogs](http://colah.github.io/)   | nice tutorials for AI|
| 5   | [Jupyter Notebook Keyboard Shortcuts](https://cheatography.com/weidadeyue/cheat-sheets/jupyter-notebook/)   |cheet sheet|
| 6   | [Using git](https://training.github.com/downloads/zh_CN/github-git-cheat-sheet/)，[Resources to learn Git](https://try.github.io/)  |cheet sheet|
| 7   | [Using conda](https://kapeli.com/cheat_sheets/Conda.docset/Contents/Resources/Documents/index)，[official guide](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html)  |cheet sheet|




## Books
The online **books and blogs**:

| No.   | books and blogs                                  | Links           |
| :----:| :----:                                                  | :----:          |
| 1     | Neural Networks and Deep Learning by M. Nielsen   | [online](http://neuralnetworksanddeeplearning.com/)|
|2    |  Deep Learning by Ian Goodfellow    | [online](https://github.com/janishar/mit-deep-learning-book-pdf/blob/master/complete-book-bookmarked-pdf/deeplearningbook.pdf/), [中文](https://github.com/exacity/deeplearningbook-chinese)|
| 3   | Deep Learning with PyTorch (official guide book)  | [PDF](https://pytorch.org/assets/deep-learning/Deep-Learning-with-PyTorch.pdf)|


More (100+) free **AI books** [online](https://www.theinsaneapp.com/2020/12/download-free-machine-learning-books.html):
<div>
    <div style="text-align:center">
    <img width=99%device-width src="doc/Free_Books.jpg">
</div>



## Common issues

**create a new env in anaconda (win10)**  
by following commands in 'anaconda prompt' or 'cmd' or 'VS code terminal (bash)':
```
conda info -e # check current env
conda create --name my_env # an empty env named my_env 
conda activate my_env # if fail in VS code terminal (bash), see issue below 
conda install package_name
conda install pip # Must do this before using pip! see reason below！
pip install package_name # pip may support more packages than conda
``` 
安装特定版本的包　conda用“=”，pip用“==”:
```
conda install numpy=1.93
pip install numpy==1.93
```

**Note: pip不知道当前环境**，我们首先要确保我们用的是本环境的pip，这样pip install时，包才会创建到本环境中，不然包会创建到base环境，供各个不同的其他conda环境共享，此时可能会产生版本冲突问题!
在当前环境下，用下面bash命令查看将要用的pip 为哪个环境：
```
which -a pip 
```
在新建立的env下，做一个小实验，确保pip把一个（不太常用的）包（folium）only安装在本env中（而不是base环境中）：
```
pip install folium # package visualizing geospatial data
conda list
conda deactivate
conda info -e 
conda list
```
conda list结果中，pip安装的包的build标注为pypi. 退出新env后回到base环境，conda list中应该不会出现folium. 否则，可能是误用了base环境下的pip，所以包被安装到base环境中（may conflict）.


**Can't execute 'conda activate' from bash (win10 + terminal of VS code)**
```
eval "$(conda shell.bash hook)"
conda activate my_env
``` 

**Create an env for tf2.2-GPU (win10)**  
tf 2.2 (2.3 and higher do not work with my CUDA) requres python 3.5-3.8, CUDA 10.1, cuDNN 7.6, more version infor at [here](https://www.tensorflow.org/install/source#tested_build_configurations). Somehow only py3.7 works well with tf2.2-GPU.
```
conda create -n py37_tf2.2 python=3.7 anaconda # 'anaconda' enables a full copy from the base env
conda activate py37_tf2.2
pip install tensorflow-gpu==2.2
```

以下命令区别是：前者建立一个空的环境，后者把base环境完整复制过来，里面已经包括了常用的包如pip，numpy
```
conda create --name my_env
conda create --name my_env anaconda
```
