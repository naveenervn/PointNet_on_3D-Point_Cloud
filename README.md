# PointNet_on_3D-Point_Cloud
 Implementation of PointNet NN for Object recognition on 3D Point Cloud using ModelNet10 Dataset. Achieved 83% Accuracy.

## How to Run:
	1.The python code is available as .ipynb files.
	2.There are 2 files
		a. main.ipynb 	- Contains the main code for preprocessing and training program
		b. plots.ipynb	- Contains various visualisations used for exploring given dataset(used prior to main.ipynb)

	3.Hence open the codes in jupyter notebook, install dependancies and libraries provided in the notebook if necessary.
		installations codes are available as '!pip install ' lines.
	4.Copy path of extracted ModelNet10 directory in path = "*/ModelNet10" (assuming ModelNet10.zip is extracted)
	5.Run the code cell by cell till end.

## 3D Point cloud and PointNet
 A point cloud is a collection of points in a 3D space, where each point represents a specific coordinate (x, y, z) in the environment. Point clouds are commonly generated    using 3D scanning techniques such as LiDAR (Light Detection and Ranging) or photogrammetry.

 PointNet is a deep learning architecture specifically designed for processing point clouds. It takes as input a set of unordered points and directly operates on them,        without requiring any intermediate representation such as voxels or meshes. This makes PointNet particularly suitable for handling irregular and unstructured data.
  	
  ### 1.Input Representation:
The input to PointNet is a set of points representing a 3D object or scene. Each point is represented by its (x, y, z) coordinates, and optionally, 			additional features such as color or intensity values.
  ### 2.PointNet Architecture:
PointNet architecture consists of several layers of neural network operations, including fully connected layers, convolutional layers, and max pooling layers.
The architecture is designed to process each point independently, followed by aggregating information across all points to generate a global representation 		of the 	entire point cloud.
  ### 3.Feature Extraction:
PointNet learns hierarchical features from the input point cloud by processing each point through multiple layers of neural network operations.
These operations help extract local geometric features from individual points as well as capture global context and shape information from the entire point 		cloud.
  ### 4.Task-specific Outputs:
Depending on the application, PointNet can be used for various tasks such as classification, segmentation, object detection, or reconstruction.
For classification tasks, PointNet typically produces a probability distribution over different classes or categories.
For segmentation tasks, PointNet assigns a label to each point indicating the part or object it belongs to.
 ![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/6f4ee997-e858-4699-9c1a-4939c05a5f44)

The above [PointNet](https://stanford.edu/~rqi/pointnet/) architecture has been followed by our code.

### Data Augmentation techniques:
- Objects come in a variety of sizes and can be positioned in various locations within our coordinate system.
- In order to improve our training, we also incorporate data augmentation techniques such as randomly rotating the object along the Z-axis and introducing Gaussian noise.
### Train and Test data split:
- 3991 models for training and 908 for testing.
- Train dataset size: 3991
- Valid dataset size: 908
- Number of classes: 10
![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/03d198b9-b078-4500-ac72-abc43e1aab20)

![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/9e43199a-d565-43e8-9446-f2b65a321b13)

![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/39aaa578-a2e0-47a1-812f-c0a007d26716)

### Code Performance:
The final prediction performance of trained model is as:
1. Number of epoch of training : 8
2. Number of batches per epoch : 125
3. Training Accuracy : 87.35 %
4. Validation Accuracy : 83.93 %
5. training loss : 0.385
6. Validation Loss : 0.477

![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/0309a8dd-3037-447b-b76f-585daa7f356e)

![image](https://github.com/naveenervn/PointNet_on_3D-Point_Cloud/assets/172423091/62496629-5723-4b6e-bb98-70d5cc511eca)

### Observation and Conclusion:
1. We have successfully implemented PointNet architecture for ModelNet10 object classification.
2. Achieved 83% accuracy in classifying 10 object categories.
3. PointNet effectively handles unordered point cloud data.
4. ModelNet10 dataset provided diverse 3D objects for training.
5. Future work may include exploring different architectures and data augmentation techniques.
### Pretrained model
Is available [here.](model_acc83.pth)

Implementation by Naveen Raja Elangovan
