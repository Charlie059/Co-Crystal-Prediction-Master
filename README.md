# Co-crystal Prediction Model


The use of a two-step PU learning technique enables the use of only positive samples and unlabelled data in cases where negative samples are unreliable.

## Features

- Using Spy-based PU learning techniques
- No negative samples are used
- Powerful ability to find positive data in unlabelled samples



> As a general rule, in co-crystal synthesis experiments we cannot fully identify negative samples because the experiment depends on the specific method, solubility of the material, temperature of synthesis, etc. Therefore it is not feasible to model the data using only the traditional binary classification. Instead, we used the PU learning method using only positive and unlabelled samples.



## Libraries

I strongly recommend that you use Google Colab to run the following essential libraries:

- Shap
- Numpy
- rdkit
- ccdc
- Pandas
- Sklearn
- Scipy
- Matplotlib

## Workflow

# 1. Generating the datasets:
-  Co_crystals extraction from Cambridge Crystalographic Structural Database (CSD) (Requires the installation of the CCDC Python API)
-  Designing the labeled (CSD) and unlabeled (ZINC15) dataset

# 2. Feature representation:
- Use Morderd to calculate the generated features

# 3. Data cleaning
- Data Dimensionality Reduction
- Illegal data cleansing

# 4. Data pre-processing methods (Disposed)
- Use DBSCAN to clean up outliers from positive data
- Negative data generation using SMOTE oversampling method
- Random undersampling of positive data
- Classification using the Random Forest algorithm

# 5. PU Learning
- Using a two-step approach, a reliable negative sample is first found in the unlabelled sample, and then a traditional binary classification is used
- Finding reliable negative sample RN by Spy algorithm

# 6. Evaluations
- The recall evaluation model was used because we did not know the true negative sample.
- The F1 approximation will be used in the future
- Evaluating the ability of different algorithms to find hidden positives by hiding them in unlabelled data

## License

MIT

## Reference

https://github.com/Charlie059/Co-Crystal-Prediction-Master/blob/main/Reference.txt
