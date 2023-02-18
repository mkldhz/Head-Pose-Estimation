# Head-Pose-Estimation

Head pose estimation is a machine learning project that aims to predict the orientation of a person's head in 3D space. The project involves drawing the three rotational axes of the head (pitch, yaw, and roll) by predicting the corresponding angles for each axis using machine learning models.
<p align="center">
  <img src="https://user-images.githubusercontent.com/61518213/219884122-bc4dca9b-4487-468a-90a3-8aafe7d0f050.png"/>
</p>

# Dataset
The [AFLW2000 dataset](http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/Database/AFLW2000-3D.zip) is used for this project which consists of 2000 images and 2000 matlab files which contain the three rotational axes of the head (pitch, yaw, and roll) for each image.

# Preview

https://user-images.githubusercontent.com/61518213/219885204-a7ed85f3-bb3d-4ce6-9baf-e37aefd1f87c.mp4



# Solution
The solution to the problem involved the following steps:

1 - Getting data ready, which included downloading the dataset and unzipping it

2 - Extracting Landmarks, this was done via [MediaPipe's Face Mesh Model](https://google.github.io/mediapipe/solutions/face_mesh.html)
<p align="center">
  <img src="https://user-images.githubusercontent.com/61518213/219885056-760f3b46-051e-486f-ae1a-c7204c9531d8.png"/>
</p>

3 - Extracting labels for each image

4 - Normalization, this was done by subtracting the detected landmarks from the nose point and dividng them by the distance between the forehead and the chin. The normalized landmarks represent our features.

5 - Model training, in this phase several model were trained by feeding them the featrues and labels.

6 - Model optimization, fine-tuning each model to get the least MSE and RMSE.
