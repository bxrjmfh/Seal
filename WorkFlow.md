# 印章识别

该部分代码用于提取印章，并且对差异最大的部分进行提取标识。主要分为印章提取，对比检测等。

## 入口文件 main.py

程序执行的入口，首先需要在开头输入文件所在的路径。假设输入`filepath`，那么程序将会遍历其中的所有文件夹，对正负样本输出结果，并输出其结果。filepath 中图像应该是存在多个文件夹中的，每个文件夹的内容都包含一对正负样本。

```
filepath
	|
	|--sample1
	|	|--pos.png
	|	|--neg.png
	|	
	|--sample2
	|	|--pos.png
	|	|--neg.png
	|...

result
	|--sample1_res.png/txt
	|--sample2_res.png/txt
```

## 模块文件 sealTools

包含各种所需的函数。

### 印章提取 exactionSeal.py

该部分输入图片，得到二值化的印章图像。

### 尺寸归一化