# Text-adversarial-attack-NLP3A

This work is the result of our ENSAE 3rd year NLP project. We chose the subject of detecting adversarial attacks. The method is about estimating densities of text samples to detect adversarial examples, as they tend to have a lower density than the original examples. We apply a kernel PCA and Minimum Covariance Determinant in order to have a robust density estimation. Our methods mainly rely on a paper named "paper.pdf" that we put in the repository.

# Data

Our dataset is the dataset developed by the authors of the paper. It is called "bert-base-uncased-imdb_bae.csv". You can find it here https://drive.google.com/drive/folders/1njfSzIDYtAc1xL_mAWix_MnHO2fpkBRs?usp=sharing as it is too big to upload in our repository. There are also the datasets of the other attacks.

# Robust density estimation 

In the notebook "robust_density_estimation.ipynb", we implement the robust density estimation method with the kernel PCA and the minimum covariance determinant that we mentionned above. We plot densities for some diverse text, original and adversarial. We compare the densities obtained with robust density estimation versus the simple maximum likelihood estimator. The results show a more different density between adversarial and original text, making the RDE the best density estimation.

# Model

In the "model.py" python file, we implement the whole model that returns the ROC of our RDE.

# Results

In the notebook "accuracy_results.ipynb", we show the results of our method, compared to what the MLE gives, and test it on diverse attacks. The results obtained with the Robust density estimation are satisfying, and better than the ones with MLE.
