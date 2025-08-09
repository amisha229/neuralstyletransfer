# Neural Style Transfer with PyTorch

This project implements **Neural Style Transfer (NST)** using a pre-trained VGG19 model in PyTorch.  
It blends the **content** of one image with the **style** of another to produce a new, stylized image.

## 📌 Features
- Uses **VGG19** pretrained on ImageNet.
- Fully implemented in **Google Colab** for easy execution.
- Upload custom **content** and **style** images.
- Adjustable parameters for style/content weighting and optimization steps.
- Saves and downloads the final stylized image.


## 🛠 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

🚀 How to Run
Option 1: Google Colab (Recommended)
1. Open GenAi.ipynb in Google Colab.
2. Run the first cell to install dependencies.
3. Upload:
   -Content image (base image whose structure will be preserved).
   -Style image (artwork whose style will be applied).
4. Adjust parameters if desired:
   -num_steps (default: 300)
   -style_weight (default: 1e6)
   -content_weight (default: 1)
5. Run the style transfer.
6. Download the generated image (stylized_output.png).

Option 2: Local Execution
1. Clone this repository:
```bash
Copy
Edit
git clone https://github.com/your-username/your-repo.git
cd your-repo
```
2. Install dependencies:
```bash
Copy
Edit
pip install torch==2.6.0 torchvision==0.21.0 pillow matplotlib numpy
```
3. Replace Colab upload code with local file paths for your content and style images.
4. Run the notebook in Jupyter Notebook or JupyterLab.

📂 Project Structure
```bash
Copy
Edit
GenAi.ipynb          # Google Colab notebook with full implementation
stylized_output.png  # Output image (generated after running)
README.md            # Project documentation
```

⚙️ How It Works
Preprocessing: Images are resized and converted to tensors.
Feature Extraction: VGG19 layers extract content and style features.
Loss Calculation:
 -Content Loss: Compares content features of generated vs. target image.
 -Style Loss: Compares Gram matrices of style features.
 -Optimization: Uses L-BFGS to iteratively update the generated image.


