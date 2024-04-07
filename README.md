# Basketball Goal Highlights With Computer Vision

Bachelor's thesis project in Computer Science: Artificial Intelligence at Kharkiv National University of Radio Electronics.

The main goal of this project is to create basketball highlights of goals using computer vision with two parts: YOLOv5 for identifying the basket and ResNet50 for classifying goal/no goal. 

The whole process was documented in [Serhii_Fedosov_Thesis_Basketball_Goal_Highlights.ipynb](https://github.com/askador/basketball-highlights/blob/main/Serhii_Fedosov_Thesis_Basketball_Goal_Highlights.ipynb).

I chose a basketball game [Ukraine v Poland | FIBA EuroBasket 2022](https://www.youtube.com/watch?v=05Y9a5vRIxI) to create highlights. Here are the created [clips](https://ktureedu-my.sharepoint.com/:f:/g/personal/serhii_fedosov_nure_ua/Eqsef-8A179DggS5tThUkdcB2iMu3j4uYYT80DsH8r6V2g?e=axMzLi) and [higlights video](https://ktureedu-my.sharepoint.com/:v:/g/personal/serhii_fedosov_nure_ua/EZp42USWqVpBojK9pIfEw2wBS8ol6TqfSOSyzTmSSyijzw?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=mjw216) using our models.

### Technologies

* Python
* PyTorch
* YOLOv5
* OpenCV
* MoviePy

### Results

Detection of goals does not have the greatest performance. From a video I fed to the models, we got following results:

* Goals detected: 20
* Goals not detected: 2
* Mistaken detection: 27

More than half of the detections are mistaken. Metrics we got are: **Precision**: 0.425 and **Recall**: 0.91. 

**The main problem** was not classification of goal/no goal, but the detection of the basket.

To conclude, our model has an **excellent recall**. It could be a useful tool to assist with the creation of basketball highlights. The model could suggest the timings, and we could choose to include them in the highlights or not.

Still, **half of the detections are mistaken**, it would be nice to invest some time into either using newer or more capable YOLO versions, or being careful with data and dedicate some time for manual data selection and preprocessing.  