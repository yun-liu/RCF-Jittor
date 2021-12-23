## [Richer Convolutional Features for Edge Detection](http://mmcheng.net/rcfedge/)

This is the Jittor implementation of our edge detection method, RCF.

### Citations

If you are using the code/model/data provided here in a publication, please consider citing:

    @article{liu2019richer,
      title={Richer Convolutional Features for Edge Detection},
      author={Liu, Yun and Cheng, Ming-Ming and Hu, Xiaowei and Bian, Jia-Wang and Zhang, Le and Bai, Xiang and Tang, Jinhui},
      journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
      volume={41},
      number={8},
      pages={1939--1946},
      year={2019},
      publisher={IEEE}
    }
	
### Requirements

* [Jittor](https://github.com/Jittor/jittor)
* numpy
* opencv-python
* scipy

    
### Testing

1. Clone the RCF repository:
    ```
    git clone https://github.com/yun-liu/RCF-Jittor.git
    ```

2. Download the pretrained model ([BSDS500+PASCAL](https://drive.google.com/file/d/1oxlHQCM4mm5zhHzmE7yho_oToU5Ucckk/view?usp=sharing)), and put it into the `$ROOT_DIR` folder.

3. Download the BSDS500 dataset as below, and extract it to the `$ROOT_DIR/data/` folder.

    ```
    wget http://mftp.mmcheng.net/liuyun/rcf/data/HED-BSDS.tar.gz
    ```

4. Run the following command to start the testing:
    ```
    python test.py --checkpoint bsds500_pascal_model.pth --save-dir /path/to/output/directory/
    ```
   This pretrained model should achieve an ODS F-measure of 0.812.

For more information about RCF and edge quality evaluation, please refer to this page: [yun-liu/RCF](https://github.com/yun-liu/RCF)

### Edge PR Curves

We have released the code and data for plotting the edge PR curves of many existing edge detectors [here](https://github.com/yun-liu/plot-edge-pr-curves).

### RCF based on other frameworks 

PyTorch based RCF: [yun-liu/RCF-PyTorch](https://github.com/yun-liu/RCF-PyTorch)
Caffe based RCF: [yun-liu/RCF](https://github.com/yun-liu/RCF)
