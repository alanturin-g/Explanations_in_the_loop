# Learn and streamline with explanations in the loop
Repository containing the code to run *Iterative Dataset Weighting* (IDW) and *Targeted Replacement Values* (TRV).
The **dataset** folder contains the tested datasets.
The **results IDW** folder can be used to save the results produced by IDW.
The **results TRV** folder can be used to save the results produced by TRV.

In order to run the proposed methods:
- open the notebook according to the chosen method: **IDW.ipynb** for IDW or **TRV.ipynb** for TRV;
- run the code passing to the main method the parameters according to the chosen configuration;

The parameters are the following:
- **dataset**: Name of the chosen dataset. {"cancer", "HeartRisk", "student", "kidney"};
- **data_path**: Path to the dataset folder;
- **results_path**: Path where to save the results;
- **regularizer**: Type of regularizer. {None, "l1", "l2", "l1_l2"};
- **title**: Title to append at the files names;

Results saved by the methods:
- **keras models** trained during IDW or TRV: *{n_iter}_median_model_1_hidden*;
- **history** of the keras models: *{n_iter}_median_model_1_hidden.npy*;
- **SHAP scores** computed on the train set: *{n_iter}_median_model_1_hidden.tsv* and *{n_iter}_median_model_1_hidden.png*;
- **SHAP scores** computed on the test set: *{n_iter}_median_model_1_hidden_test.tsv* and *{n_iter}_median_model_1_hidden_test.png*;
- **precision, recall, f1, XCP, AUC and accuracy**: *results {title}.tsv*;
- **confusion matrix**: *confusion matrix {title}.tsv*;

Produce the plots after producing all the results.