# mnist-resnet50-transfer-learning

This project applies transfer learning using ResNet50 (pretrained on ImageNet) to classify digits from the MNIST dataset.  
The grayscale digits are resized into 96×96 RGB images to match the ResNet50 input requirements.

The workflow includes:
- Preprocessing MNIST digits into RGB images
- Data augmentation (rotation, translation, zoom)
- Transfer learning with ResNet50 (frozen layers)
- Fine-tuning last 50 layers of ResNet50
- Training/validation/test evaluation
- Accuracy plots

#Installation

Clone the repository and install dependencies:
```bash
git clone https://github.com/Prathana-192/mnist-resnet50-transfer-learning.git
cd mnist-resnet50-transfer-learning
pip install -r requirements.txt

#Model Architecture
Base Model: ResNet50 (include_top=False, pretrained on ImageNet)
Layers:
Data Augmentation (rotation, translation, zoom)
ResNet50 backbone
GlobalAveragePooling2D
Dense(128, relu)
Dropout(0.3)
Dense(10, softmax)

#Results
Initial Transfer Learning Test Accuracy ≈ ~ (varies, typically 90%+ for subset)
After Fine-Tuning, accuracy improves further
Accuracy curves are plotted for both stages
