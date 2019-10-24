### Keras/Tensorflow 2.0 implementation of an Octave Convolution Unet for image segmentation and transposed octave convolutions

Inspired by:

    @misc{fan2019accurate,
    title={Accurate Retinal Vessel Segmentation via Octave Convolution Neural Network},
    author={Zhun Fan and Jiajie Mo and Benzhang Qiu and Wenji Li and Guijie Zhu and Chong Li and Jianye Hu and Yibiao Rong and Xinjian Chen},
    year={2019},
    eprint={1906.12193},
    archivePrefix={arXiv},
    primaryClass={eess.IV}
    }


With a few fixes from their paper to achieve better performance:  
    1) Deeper network with more parameters    
    2) Added dropout only in deepest layer  
    3) Utilizing rectified ADAM optimizer  
    4) Octave transposed H→L kernels first apply vanilla transposed convolution and then downsample output by   
    a scale of two, which better follows the rigor of the orginal octave convolution paper   

Google Colab example: https://colab.research.google.com/drive/1WcBaJMnwGIuMY_SWH3qNI5OyXd8KTYTO
    
Octave Convolutions:

    @misc{chen2019drop,
    title={Drop an Octave: Reducing Spatial Redundancy in Convolutional Neural Networks with Octave Convolution},
    author={Yunpeng Chen and Haoqi Fan and Bing Xu and Zhicheng Yan and Yannis Kalantidis and Marcus Rohrbach and Shuicheng Yan and Jiashi Feng},
    year={2019},
    eprint={1904.05049},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
    }
    
Unet:

    @misc{ronneberger2015unet,
    title={U-Net: Convolutional Networks for Biomedical Image Segmentation},
    author={Olaf Ronneberger and Philipp Fischer and Thomas Brox},
    year={2015},
    eprint={1505.04597},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
    }
