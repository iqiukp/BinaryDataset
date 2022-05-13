# 🔥🔥 BinaryDataset
 MATLAB code for 2D or 3D binary dataset.
 
## ✨ MAIN FEATURES
- 2D or 3D binary dataset of "banana" and "circle" shapes.
- Partitioning of training dataset/label and test dataset/label.

## 🔨 HOW TO USE

```MATLAB
ocdata = BinaryDataset();
[data, label] = ocdata.generate;
[trainData, trainLabel, testData, testLabel] = ocdata.partition;
```
The full Name-Value Arguments of class `BinaryDataset` are
- `shape`: shape of dataset, 'banana' or 'circle'.
- `dimensionality`: dimensionality of dataset, 2 or 3.
- `number`: number of samples per class, for example: [200, 200].
- `display`:  visualization, 'on' or 'off'.
- `noise`:  noise added to dataset with range [0, 1]. For example: 0.2.
- `ratio`: ratio of the test set with range (0, 1). For example: 0.3.

### 👉 Example 1
Generate a 3D banana-shaped dataset with 200 and 100 samples for each class, and divide 10% of the data into the test dataset.
```MATLAB
ocdata = BinaryDataset( 'shape', 'banana',...
                        'dimensionality', 3,...
                        'number', [200, 100],...
                        'display', 'on', ...
                        'noise', 0.2,...
                        'ratio', 0.1);
[data, label] = ocdata.generate;
[trainData, trainLabel, testData, testLabel] = ocdata.partition;
```
<p align="center">
  <img src="http://github-files-qiu.oss-cn-beijing.aliyuncs.com/BinaryDataset/3D_banana.png">
</p>

### 👉 Example 2
Generate a 2D circle-shaped dataset with 100 and 300 samples for each class, and divide 50% of the data into the test dataset.
```MATLAB
ocdata = BinaryDataset( 'shape', 'circle',...
                        'dimensionality', 2,...
                        'number', [100, 300],...
                        'display', 'on', ...
                        'noise', 0.2,...
                        'ratio', 0.5);
[data, label] = ocdata.generate;
[trainData, trainLabel, testData, testLabel] = ocdata.partition;
```
<p align="center">
  <img src="http://github-files-qiu.oss-cn-beijing.aliyuncs.com/BinaryDataset/2D_circle.png">
</p>

