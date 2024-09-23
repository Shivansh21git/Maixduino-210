Facial Recognition Project with Maixduino Sipeed Board
Introduction
This project involves facial recognition using the Maixduino Sipeed Board, leveraging a model trained on the MaixHub platform. The dataset is collected using the GC0328 camera module, which captures images and feeds them to the model for real-time facial recognition. This project aims to demonstrate how powerful edge AI can be for applications like security, smart devices, and more.
Project Components
- **Maixduino Sipeed Board**: The core processing unit for facial recognition, powered by the Kendryte K210 RISC-V AI processor.
- **GC0328 Camera**: Captures real-time images for dataset collection and facial recognition.
- **MaixHub Platform**: Used for model training and deployment.
- **SD Card**: Stores the model and captured data.
Setup Instructions
1. **Collect Dataset**: Use the GC0328 camera to capture images for training. Ensure the images are clear and well-lit.
2. **Model Training**: Visit the MaixHub platform and upload the dataset. Train the model with the appropriate parameters for facial recognition.
3. **Model Deployment**: Once the model is trained, deploy it to the Maixduino Sipeed Board by copying the model to an SD card and inserting it into the board.
Code Usage
To get started with the project, you can use the provided Python code to interface with the Maixduino and run the facial recognition tasks.
Example Code
```python
import sensor, image, lcd, time
from Maix import KPU

# Initialize the camera
sensor.reset()
sensor.set_pixformat(sensor.RGB565)
sensor.set_framesize(sensor.QVGA)
sensor.skip_frames(time=2000)

# Load the trained model
task = KPU.load('/sd/facedetect.kmodel')
```

Contributing
Feel free to contribute to this project by submitting issues or making pull requests. Whether it's optimizing the model, adding new features, or improving the overall performance, contributions are always welcome!
