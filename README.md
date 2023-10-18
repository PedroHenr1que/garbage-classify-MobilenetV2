# Garbage Classification With MobilenetV2

This project aims to develop a model designed for integration into an intelligent waste bin. The model's primary function is to categorize different types of waste, ensuring they are correctly sorted into the appropriate bins.

## Description

In this project, we employ the MobilenetV2 architecture to construct a waste classification model. The aim is to streamline waste segregation and recycling processes, thereby contributing to the reduction of environmental impact. We also used garbage images that we found on Kaggle to train the model.

## Requeriments
- python
- numpy
- pandas
- matplotlib
- seaborn
- tensorflow
- keras
- Pillow
- scikit-learn

You can use the following command to install all the requirements and than you should be ready to go.
```python
pip install -r requirements.txt
```

## How to Use

You can simply load the file "garbage_class_model.h5" and start the prediction.

```python
model = tf.keras.models.load_model("garbage_class_model.h5")
``` 
You also can also put the images you want to predict in the "self_images" folder and run the last cell of the notebook.

## The Training Process

We chose a garbage database with more than 15,000 categorized images of items that are usually discarded in a trash bin. We found this database on Kaggle, and the categories include battery, biological, glass, cardboard, clothes, metal, paper, plastic, shoes, and trash. The model was trained for 7 epochs. Here are the results:

![Training Results](https://github.com/PedroHenr1que/garbage-classify-MobilenetV2/assets/79605051/9e1edb47-4b4f-4a31-bff9-c7e3623f23cd)

## Avaliation

The model's results are excellent, with an accuracy of more than 90%.

![Model Accuracy](https://github.com/PedroHenr1que/garbage-classify-MobilenetV2/assets/79605051/9df8a7bf-7813-4dac-9c6d-41688f0fb891)

The Clothes class has many more images, which significantly influences the accuracy because the F1-Score is very high. To address this problem, it's best to consider the Macro AVG, as it's less influenced by the Clothes class value. We've also plotted the Confusion Matrix.

![Confusion Matrix](https://github.com/PedroHenr1que/garbage-classify-MobilenetV2/assets/79605051/6ffc7979-d9d7-471b-b8f7-c84e46a63de5)

## Testing With Images That I Took
I took some pictures of things that I usually throw in the tash so I could see if the model was predicting them properly. Here it the prediction, it got everything right.

![Testing with Self-Taken Images](https://github.com/PedroHenr1que/garbage-classify-MobilenetV2/assets/79605051/f8170a1d-2b91-4ea4-b225-fd6814099304)

## References 
- Kaggle Image Database: [Garbage Classification Dataset](https://www.kaggle.com/datasets/mostafaabla/garbage-classification/data)
- Kaggle Notebooks About How to Use MobilenetV2: [Kaggle Notebooks](https://www.kaggle.com/code/rajanbirsingh/garbage-classification)
- About MobilenetV2: [Google Blog](https://blog.research.google/2018/04/mobilenetv2-next-generation-of-on.html)
- Smart Trash Bin Research Paper: [Research Paper](https://arxiv.org/pdf/2208.07247.pdf)
