## Project: Perception Pick & Place

---

In order to complete the project, the main procedures are described as following: 

1. The cloud points are processed to remove noise. 
![image1](writeup_images/ex11.png)
2. Objects that we are intersted in are seperated from the table in this case by filtering points in axis z direction. 
![image2](writeup_images/ex13.png)
3. Each object(highlighted in different colors) is then extracted using RANSAC algorithm. Now Each object is ready to be classified. 
![image3](writeup_images/clustering.png)
4. Training dataset is generated. The initial training result with random feature engineering is shown below. As you can see, the prediction accuracy is **0** for all the items. This is simply another example of "Garbage in, Garbage out". 
![image4](writeup_images/untrained_table.png)
5. Feature engineering. Since our objects are relavitely simple, only two features are extracted in this project. One is color histgram, and the other one is shape of normals on the object. Using these features, accuracy was improved to 80% to 96%. This accuracy can be futher improved by taking more training data, and do a more sophisiticated feature engineering. 
![image4](writeup_images/perception.png)

6. After the classifier is trained, it is applied to recognize the objets appear in the Perception project. 
![image4](writeup_images/objects.png)


## Summary and what to do next: 
This project is quite rewarding. It helps me understand how to process, analyze cloud points data, and make predictions using classified I just trained step by step in practice.

Although I completed the project by following the instructions provided by Udacity, there are much more left that I'd like explore. For example, how to modify the robot using xarco, specify details of the models using launch, and control the robot as wanted with scripts. 



