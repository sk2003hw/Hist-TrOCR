# Hist-TrOCR  
Fine-tuned TrOCR on Historical Text (from [the ARDIS Dataset](https://ardisdataset.github.io/ARDIS/)- Part I and [the Washington Database](https://fki.tic.heia-fr.ch/databases/washington-database)- line and word images). The model is deployed on HuggingFace ([here](https://huggingface.co/sk2003/hist-trocr)) and as a [Space](https://huggingface.co/spaces/sk2003/Hist-TrOCR) for testing it out. [IAM Handwriting Database](https://fki.tic.heia-fr.ch/databases/iam-handwriting-database) has been used in to compare this finetuned model with the original TrOCR as the latter was trained on this dataset.  

The Jupyter notebook can be downloaded and run using any compatible IDE or viewed from [this link](https://colab.research.google.com/drive/11vWXRLM4gz9h5hFpPRR_DEgd7U-t9ZVp?usp=sharing). The data has to be downloaded from the previously attached links or from [here for the ARDIS Dataset](https://drive.google.com/drive/folders/1EN0hbqE1EjXCp6jZVqB-7DdWPTvDk63a?usp=sharing), [here for the Wasington Database](https://drive.google.com/drive/folders/1I2s3rrfOKncPAamB6PCL7cSwe1ykHk_d?usp=sharing) and [here for the IAM Handwriting Database](https://drive.google.com/drive/folders/1n7ePKEf4v1Z_B_w99dQnl6ij7giEPjnf?usp=sharing). To run the Colab notebook, the datasets have to be saved in Google Drive and the path of the data and the ground truth files have to be updated in the code depending on the location of the data in your Google Drive. The file names should remain the same but the directories’ names could change so this has to be kept in mind. If the code is run on your local machine, additional libraries must be installed using pip. These are given in the ‘Setup’ section of the notebook and also mentioned below.   

### Pip Downloads to make
pip install transformers # Transformers library from HuggingFace   
pip install torch # PyTorch framework  
pip install jiwer # for loading CER metric  
pip install evaluate # from HuggingFace; to use the CER metric for evaluation  
pip install -q gradio # to create an interactive demo of the model  

### ARDIS Dataset  
Files used are- Part I.xlsx for the ground truth and 'Part I' folder for the images.  

### Washington Database  
Files used are- ground_truth/ground_truths.csv for the ground truths and data/line_and_word_images_normalized for the images.  

### IAM Handwriting Database
Files used are- gt_test.txt for the ground truth and 'image' folder for the data.  
