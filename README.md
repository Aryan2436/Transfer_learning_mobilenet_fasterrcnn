# Transfer Learning with MobileNet & Faster R-CNN

A computer vision project demonstrating **transfer learning with PyTorch and Torchvision** for image classification and object detection. The notebook compares a lightweight MobileNet model with Faster R-CNN object detectors.

## Project Overview

This project is organized into three parts:

| Part | Model | Task | Dataset |
|---|---|---|---|
| A | MobileNet V2 | Image classification: ants vs. bees | Hymenoptera |
| B | Faster R-CNN with ResNet-50 FPN backbone | Pedestrian detection | Penn-Fudan Pedestrian |
| C (Bonus) | Faster R-CNN with MobileNet V3 Large FPN backbone | Pedestrian detection | Penn-Fudan Pedestrian |

## Key Concepts

- **Transfer learning:** starts from a model pretrained on a larger dataset and adapts it to a new task.
- **Feature extraction:** freezes MobileNet V2's pretrained feature extractor and trains a new classification head.
- **Fine-tuning:** allows pretrained model layers to update during training.
- **Object detection:** predicts object classes and bounding boxes in images.
- **Model comparison:** demonstrates a Faster R-CNN detector using a ResNet-50 FPN backbone and a lighter MobileNet-based backbone.

## Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Pillow (PIL)
- Jupyter Notebook / Google Colab

## Datasets

The notebook downloads the datasets automatically when the relevant cells are run.

1. **Hymenoptera (ants vs. bees)**  
   Used for the MobileNet V2 classification task.  
   Dataset: https://download.pytorch.org/tutorial/hymenoptera_data.zip

2. **Penn-Fudan Pedestrian**  
   Used for pedestrian detection with Faster R-CNN.  
   Dataset: https://www.cis.upenn.edu/~jshi/ped_html/PennFudanPed.zip

Please review each dataset's terms and attribution requirements before redistributing it.

## Run the Project

### Option 1: Google Colab

1. Open the notebook in Google Colab.
2. Select **Runtime → Run all**, or execute the cells in order.
3. If prompted, allow the notebook to download the datasets.
4. Review the training logs and displayed prediction visualizations.

**Google Colab notebook:**  
[Open the notebook](https://colab.research.google.com/drive/1HUvSAjEkRle3lT4nvLw_AjflD97JTcj_?usp=sharing)

You may need to sign in to Google and save a copy to your Drive, depending on the notebook's sharing permissions.

### Option 2: Run Locally

1. Clone or download this repository.
2. Install Python and the required libraries.
3. Launch Jupyter Notebook and open the `.ipynb` file.
4. Run the notebook cells in order.

Install the main dependencies with:

```bash
pip install torch torchvision matplotlib pillow numpy jupyter
```

For best compatibility, install a PyTorch build suited to your operating system and hardware by following the official instructions: https://pytorch.org/get-started/locally/

The notebook selects an available compute device in its setup code. A CUDA-capable GPU can help reduce training time, but a CPU may also be used.

## Repository Structure

```text
.
├── README.md
└── transfer_learning_mobilenet_fasterrcnn_(1).ipynb
```

You can rename the notebook to a shorter filename, such as `transfer_learning_mobilenet_fasterrcnn.ipynb`, before committing it, and update the structure above accordingly.

## Expected Outputs

When the notebook runs successfully, it is designed to show:

- A batch of sample images from the ants-and-bees dataset.
- Training and validation progress for MobileNet V2 classification.
- Ants-versus-bees classification predictions.
- Training progress for Faster R-CNN pedestrian detection.
- Pedestrian bounding-box visualizations for the ResNet-50 FPN and MobileNet-based detectors.

Actual accuracy, loss, and detection results depend on the runtime, training execution, and model weights. Refer to the notebook output for measured results.

## Notes

- The notebook uses pretrained model weights, so an internet connection may be required the first time it runs.
- Training time depends on the selected device and runtime.
- The bonus MobileNet-based Faster R-CNN section reuses the pedestrian-detection data and training loop.

## Author

**Aryan Chandrakar**

## License

No project license has been specified. Add a license file if you intend to define how others may use, modify, or distribute this project.
