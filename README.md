Internal waves play a crucial role in ocean mixing and climate modeling, but are hard to detect. This project leverages deep learning models to automate the detection process using Sentinel-1 SAR imagery.

Models Used:
1. MLP (Multi-layer Perceptron)
2. Custom CNN
3. ResNet-34
4. ResNet-50
5. YOLOv10 (object detection)
6. Faster R-CNN (object detection)

| Model         | Type             | Architecture Highlights       |
|---------------|------------------|-------------------------------|
| MLP           | Classification   | Dense Layers with ReLU        |
| Custom CNN    | Classification   | 3 Convolutional Blocks + FC   |
| ResNet-34     | Transfer Learning| Pretrained on ImageNet        |
| ResNet-50     | Transfer Learning| Higher depth model            |
| YOLOv10       | Object Detection | Real-time single-shot detector|
| Faster R-CNN  | Object Detection | Region proposal based network |

Dataset : 

* Source: Sentinel-1 SAR Imagery (Kaggle Dataset)
* Images: 4,000+ (RGB + Alpha channel, 539×528 resolution)
* Classes: Binary (Internal Wave Present = 1, Absent = 0)
* Balanced: 50/50 class distribution
* Augmentations: Rotation (90°, 180°, 270°)

### How to Run:

1. Clone the Repository :
   git clone https://github.com/yourusername/internal-waves-detection.git
   cd internal-waves-detection

2. Install Dependencies:
   pip install -r requirements.txt

3. Run the Jupyter Notebooks from the Notebooks folder OR Run the pretrained models from the Models folder:
   Example (PyTorch - ResNet-34) 
   // Load the pretrained model <br>
   model = torch.load('Models/resnet34_trained.pth') <br>
   model.eval()

### Results Summary
