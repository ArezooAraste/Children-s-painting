
Child Talent Checker

Child Talent Checker is a deep learning project that analyzes children's drawings to assess their artistic talent. Using a Convolutional Neural Network (CNN) built with TensorFlow, the model classifies drawings into two categories: "Talented (Creative)" or "Not Talented (Non-Creative)." The project features an interactive user interface powered by Gradio, allowing users to upload drawings and receive predictions with confidence scores.



## Features

Drawing Classification: Automatically evaluates children's drawings for artistic talent.



Dataset: Utilizes the Children Drawings dataset from Kaggle.



Deep Learning Model: CNN implemented with TensorFlow/Keras, achieving 84.85% test accuracy.



Interactive Interface: Upload drawings and view results via a Gradio web interface.



Open Source: Fully documented and extensible for developers.


## Prerequisites
To run this project, you need:





Python: Version 3.11 or higher



Environment: Jupyter Notebook or Google Colab



Recommended Hardware: GPU for faster model training (optional)



Dataset: Access to the Kaggle dataset (requires API key)



Python Packages:





tensorflow>=2.10



gradio>=5.0



numpy



pandas



kaggle



pillow
## Installation

1. Clone the Repository

Clone the project from GitHub:

```bash
git clone https://github.com/<your-username>/child-talent-checker.git
cd child-talent-checker
```
2. Install Dependencies

Install required packages using the requirements.txt file: 

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install tensorflow gradio numpy pandas kaggle pillow jupyter
```

3. Configure Kaggle API

To download the dataset:





Go to your Kaggle account, navigate to Account > API, and click "Create New API Token." This downloads a kaggle.json file.



Copy the file to ~/.kaggle/ (on Windows: C:\Users\<YourUsername>\.kaggle\).



On Linux/Mac, set file permissions:
```bash
chmod 600 ~/.kaggle/kaggle.json
```
4. Download the Dataset

Download and extract the dataset from Kaggle:
```bash
kaggle datasets download -d babyhackershal2020/children-drawings
unzip children-drawings.zip -d children_drawings
```
5. Run the Project
Launch Jupyter Notebook:
```bash
jupyter notebook
```
Open the Children's_painting.ipynb file.



Execute the cells in order to train the model (or load the pre-trained model) and start the Gradio interface.



Open the Gradio link (typically http://localhost:7860) in your browser.

## Project Structure

```
child-talent-checker/
├── Children's_painting.ipynb  # Main Jupyter Notebook
├── my_talent_model.h5         # Trained model (generated after running)
├── children_drawings/         # Extracted dataset directory
├── requirements.txt           # List of required packages
├── README.md                 # This file
└── sample_output.png         # Sample output image (optional)
```
## Usage
Train the Model (Optional):





To train the model from scratch, run the training cells in the notebook.



Note: This requires a GPU and may take several minutes to hours.



Use the Pre-trained Model:





Load the my_talent_model.h5 file to make predictions without retraining.



Gradio Interface:





After running the final cell, open the Gradio link.



Upload a child's drawing (JPG or PNG format).



View the prediction (e.g., "Talented (Creative)" or "Not Talented (Non-Creative)") and confidence score.



## Sample Output
Talent Prediction: Talented (Creative)
Confidence: 0.78

## Limitations
Limited Dataset: The dataset contains a finite number of drawings, which may reduce accuracy for diverse styles.



Model Format: The model is saved in the legacy HDF5 format. Future versions will use the .keras format.



Kaggle Dependency: Requires a Kaggle account and API key to download the dataset.

## Future Improvements
Expand the dataset with more diverse drawings to improve model accuracy.



Implement advanced models like ResNet or Vision Transformers.



Enhance the Gradio interface with features like input image display or detailed drawing analysis.



Add multi-language support for the user interface.



Migrate to the .keras format for better compatibility with newer TensorFlow versions.

## Contributing

We welcome contributions! To contribute:





Fork the repository.



Create a new branch for your feature:



```bash
  git checkout -b feature/your-feature
```
Commit and push your changes:
```bash
  git commit -m "Add your feature"
  git push origin feature/your-feature
```
Submit a Pull Request with a detailed description of your changes.
Please check existing Issues or create a new one before contributing.

## Troubleshooting
Dataset Download Error: Ensure your kaggle.json file is valid and you have an active internet connection. Regenerate the API token if needed.



Model Loading Error: Verify that my_talent_model.h5 exists in the project directory.



Gradio Issues: If the link doesn’t work, check if port 7860 is in use or use interface.launch(share=False) for a local server.

## License

[MIT](https://choosealicense.com/licenses/mit/)



## Acknowledgements

Thank you for using Child Talent Checker! This project was created with passion to help discover children's artistic talents.



## Contact
For questions, suggestions, or bug reports, reach out via email at arezooaraste7@gmail.com or open an issue in the Issues section.

Built with ❤️ by [Arezoo Araste]