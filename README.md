# Neural Style Transfer with VGG-19

A Python implementation of neural style transfer using two distinct approaches to compare performance and output quality.

## Overview

This repository implements neural style transfer algorithms using two different methodologies:

1. **Custom Implementation**: Building the algorithm from scratch using TensorFlow's linear algebra functions, following Gatys et al.'s original approach with VGG-19 convolutional layers
2. **Pre-trained Model**: Using TensorFlow Hub's pre-trained neural artistic stylization network proposed by Ghiasi et al.

The project compares the outputs and performance of both implementations to evaluate their effectiveness.

## Sample Output

![vgg_transform_bow_bridge_trim2](https://user-images.githubusercontent.com/8759492/150892629-d417f539-01af-4945-a18c-4cb35f399a08.gif)

## Project Structure

```
├── images/
│   ├── content/          # Content images for style transfer
│   ├── style/            # Style reference images
│   └── stylized_output/  # Generated stylized images
├── notebooks/
│   └── Neural_Style_Transfer_Base_Implementation.ipynb
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.7+
- TensorFlow 2.x
- Jupyter Notebook
- GPU support recommended for faster processing

### Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/Neural_Style_Transfer_VGG19.git
cd Neural_Style_Transfer_VGG19
```

2. Install required dependencies:
```bash
pip install tensorflow tensorflow-hub jupyter matplotlib numpy pillow
```

### Docker Usage

**Note**: Currently, no Dockerfile is present in this repository. To run this project with Docker, you would need to:

1. Create a Dockerfile with the appropriate Python environment and dependencies
2. Build the Docker image
3. Run the container with volume mounts for the images directory

If you have a Dockerfile, you can run:
```bash
# Build the image
docker build -t neural-style-transfer .

# Run the container
docker run -it -v $(pwd)/images:/app/images neural-style-transfer
```

### Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook notebooks/Neural_Style_Transfer_Base_Implementation.ipynb
```

2. Follow the step-by-step instructions in the notebook

3. Explore the generated stylized images in the `/images/stylized_output/` folder

## Additional Resources

- [Blog Post](https://philippeheitzmann.com/2022/01/implementing-vgg19-and-custom-built-style-transfer-algorithms-to-artificially-stylize-images/) - Detailed implementation walkthrough
- [Open in Colab](https://colab.research.google.com/github/philippe-heitzmann/Neural_Style_Transfer_VGG19/blob/main/Neural_Style_Transfer_Base_Implementation.ipynb) - Run directly in Google Colab
