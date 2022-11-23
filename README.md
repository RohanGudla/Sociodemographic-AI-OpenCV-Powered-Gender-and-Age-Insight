# Gender and Age Detection

This project aims to build a gender and age detector that can approximate the gender and age of a person's face in a picture or through a webcam. The project uses deep learning techniques and pre-trained models by Tal Hassner and Gil Levi.

## About the Project

In this Python project, deep learning is used to accurately identify the gender and age of a person from a single image of their face. The predicted gender can be either 'Male' or 'Female', and the predicted age falls into one of the following ranges: (0 – 2), (4 – 6), (8 – 12), (15 – 20), (25 – 32), (38 – 43), (48 – 53), (60 – 100) (8 nodes in the final softmax layer). The project formulates age prediction as a classification problem rather than regression due to the difficulty of predicting an exact age from a single image.

## Dataset

The project utilizes the Adience dataset, which is available in the public domain and can be found [here](https://www.kaggle.com/ttungl/adience-benchmark-gender-and-age-classification). This dataset serves as a benchmark for face photos and includes various real-world imaging conditions such as noise, lighting, pose, and appearance. It contains a total of 26,580 photos of 2,284 subjects in eight age ranges and is approximately 1GB in size. The pre-trained models used in the project have been trained on this dataset.

## Additional Python Libraries Required

Before running the project, make sure you have the following dependencies installed:

- `opencv-python` (install with `pip install opencv-python`)
- `argparse` (install with `pip install argparse`)

## Usage

To use this project, follow these steps:

1. Download the repository.
2. Open your Command Prompt or Terminal and navigate to the folder where all the project files are located.
3. To detect the gender and age of a face in an image, use the following command:

   ```bash
   python detect.py --image <image_name>
   ```

   Replace `<image_name>` with the name of the image you want to analyze. The image should be present in the same folder as the project files.

4. To detect the gender and age of a face through the webcam, use the following command:

   ```bash
   python detect.py
   ```

   Press `Ctrl + C` to stop the program execution.

The project will provide you with the predicted gender and age based on the input image or webcam feed.

## Working

[![Watch the video](https://img.youtube.com/vi/ReeccRD21EU/0.jpg)](https://youtu.be/ReeccRD21EU)

## Examples

Here are some examples of running the project:

- Detecting gender and age of a girl:
  ```
  > python detect.py --image girl1.jpg
  Gender: Female
  Age: 25-32 years
  ```

- Detecting gender and age of a boy:
  ```
  > python detect.py --image kid1.jpg
  Gender: Male
  Age: 4-6 years
  ```

- Detecting gender and age of a man:
  ```
  > python detect.py --image man1.jpg
  Gender: Male
  Age: 38-43 years
  ```

These examples demonstrate how the project can predict gender and age based on input images.