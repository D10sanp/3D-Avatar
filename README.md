🧠 2D to 3D Depth-Based Avatar Generator

This project converts a 2D image (like Heart.png) into a 3D mesh model using a depth estimation neural network and displays it in an interactive 360° 3D viewer.
It uses the GLPN (Global-Local Path Network) model from Hugging Face for depth prediction and Plotly + Trimesh for visualization.

🚀 Features

✅ Predicts a depth map from a single 2D image using a pretrained GLPN model.

✅ Builds a 3D mesh with realistic vertex coloring.

✅ Provides a fully interactive 360° 3D viewer (rotatable model).

✅ Works entirely in Python with Jupyter Notebook or Google Colab.

🧰 Requirements

Install the required libraries before running the script:

pip install torch torchvision torchaudio
pip install transformers
pip install pillow numpy matplotlib plotly opencv-python trimesh

🧠 Model Used

The script uses the GLPN-nyu model from Hugging Face:

Model: vinvino02/glpn-nyu

Task: Monocular Depth Estimation

Framework: PyTorch + Transformers

🧩 How It Works

Load Image:
Loads your input 2D image using PIL and resizes it.

Depth Prediction:
The GLPN model estimates pixel-wise depth values.

Depth Normalization:
The depth map is normalized and smoothed for better 3D quality.

Mesh Construction:
A 3D mesh is generated from RGB and depth data using Trimesh.

3D Visualization:
The mesh is rendered as an interactive Plotly 3D model with a rotating 360° animation.

🎥 Example Output

Predicted Depth Map:


3D Mesh Viewer:
Interactive model rotates in 360°, showing depth-based geometry.

⚙️ Run the Code

Run the following in your Jupyter Notebook or Python script:

python 2D_3D.py
