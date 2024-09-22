# Project: Assessing Biological Aging Through Machine Learning: The Impact of a Long-term Fasting-mimicking Diet
------------------------------------------------------------------

* Requires Python 3.11

### To run the custom clock:

- First, run exploratory_analysis.ipynb to get the common_cpg.npy file. This file contains the CPG sites common between the buchinger dataset and the CFFFPrize.

- Next, run kaggle_set.ipynb. Make sure to download from https://emea.support.illumina.com/downloads/infinium-methylationepic-v1-0-product-files.html the Infinium MethylationEPIC v1.0 B4 Manifest File (CSV Format) in order to be able to run kaggle_set.ipynb, change the location from mapping_info = pd.read_csv("C:/Users/amroa/aging/infinium-methylationepic-v10-b4/MethylationEPIC_v-1-0_B4.csv", skiprows=7) to where it is saved in your computer. 

- Inside kaggle_set.ipynb, train_loc, map_train_loc refers to the training data location and training data labels, respectively from the kagggle dataset https://www.kaggle.com/datasets/marquis03/age-assessment-and-disease-risk-prediction/data. Likewise, for the test data. Make sure to modify these variables to point to where they are stored on your computer. 

- Next, run kaggle_training.ipynb. Likewise, change map_train_loc = "D:/archive/ai4bio_trainset/trainmap.csv" to reflect where the CFFFPrize is on your computer. This notebook will also be used for generating age inferences on the Buchinger cohort, hence you will need to run it again (as marked in the notebook) after running cfffprize_buchinger.ipynb.

- Once you have run cfffprize_buchinger.ipynb go back to running the last section of kaggle_training.ipynb to get the Buchinger ages. 

- Finally, you can now run the last section of exploratory_analysis.ipynb. 

## Dependencies

| Library        | Version  |
|----------------|----------|
| pandas         | 2.2.3    |
| numpy          | 1.26.1   |
| scipy          | 1.11.2   |
| matplotlib     | 3.7.2    |
| scikit-learn   | 1.3.0    |
| seaborn        | 0.12.2   |
| csv            | 1.0      |
| cycler         | 0.10.0   |
| joblib         | 1.3.2    |
| json           | 2.0.9    |
