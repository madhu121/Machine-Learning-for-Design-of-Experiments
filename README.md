# Exploratory Data Analysis for Design of Experiments

This Jupyter notebook is dedicated to exploratory data analysis (EDA) with the goal of suggesting initial molecules for a theoretical experiment. It uses various techniques to explore the molecular search space.

The dataset comprises two main files:
- molecules_rdkit.csv - describes different molecules and their characteristic properties.
- molecules_results.csv - describes "damage" and "performance" metrics for all these molecules obtained from a hypothetical experiment.

The notebook addresses the following three scenarios:

1. **Candidate Selection**: 
   - The objective is to select the first 20 molecules for the experiment, ensuring a broad and efficient sampling of the latent feature space. Recommendations for the initial 20 molecules are based solely on the data provided in `molecules_rdkit.csv`.
   
2. **Predictive Model Assessment**:
   - Considering the expense of the experiment, it's crucial to assess whether the first 20 iterations are adequate for building predictive models for the outcomes. We utilize the results obtained for the selected molecules from `molecules_results.csv` to train models for estimating both "performance" and "damage," addressing this question.

3. **Optimized Sampling**:
   - Irrespective of the findings from question 2, the aim is to leverage the first 20 trials to target samples that maximize "performance" and minimize "damage" (both objectives are equally important). Models trained in question 2 are employed to evaluate the entire set of molecules, utilizing a ranking strategy to select the next 20 molecules for the experiment.
   <br/>

The supporting_info.docx presents underlying logic/explanation behind solution for each of these questions.
