# Introduction to AI: Predicting Tsunami Alerts from Earthquake Observations

This tutorial is a beginner-friendly walk through the complete machine learning workflow, using real earthquake data from the US Geological Survey. By the end, you will have built and evaluated a model that flags earthquakes likely to trigger a tsunami, while learning every concept from the ground up.

Author:
- [Tarini Bhatnagar](https://www.linkedin.com/in/tarinibhatnagar), Senior Solutions Architect AI, NVIDIA

## Access this tutorial

We recommend executing this notebook in a Colab environment to gain access to GPUs and to manage all necessary dependencies. 

<a target="_blank" href="https://colab.research.google.com/github/climatechange-ai-tutorials/intro-ai-tsunami-alerts/blob/main/Predicting_Tsunami_Alerts_from_Earthquake_Observations.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### The following four sections (## Exercise results, ## What I learned, ## My contributions, and ## Key takeaways) are my own reflections and notes after finishing the tutorial.

## Exercise results 

- Logistic Regression prioritized detection, reaching **95.2% recall** on the test set, but with **26.5% precision**.
- The Random Forest challenge achieved the best test **F1 score of 0.535**, improving on Logistic Regression's 0.415.
- Shallow depth and high magnitude were the strongest tsunami predictors, consistent with the underlying physics.
- Magnitude regression improved RMSE from **0.591** (mean baseline) to **0.469**, with an **R² of 0.370**.

## What I learned

- Accuracy alone is misleading for imbalanced safety-critical problems; recall, precision, F1, and the confusion matrix provide a more useful view.
- Threshold selection is an operational trade-off between missed events and false alarms.
- Stratified train, validation, and test splits help produce fair comparisons and reduce leakage risk.
- Strong training performance does not guarantee generalization; regional and rare-event results need careful interpretation.

## My contributions

- Completed the end-to-end workflow: exploration, preprocessing, feature engineering, baselines, model training, evaluation, and interpretation.
- Extended the notebook with configurable regional modeling and safeguards for sparse or single-class data.
- Added a magnitude-regression challenge with baseline comparison, holdout metrics, and diagnostic visualization.
- Documented the reflection exercises and practical limitations of using ML for tsunami alerts.

## Key takeaways

- ML can support rapid risk triage, but it should complement physical models, real-time sensors, and expert review.
- Model selection must reflect the cost of errors; for tsunami alerts, reducing false negatives is especially important.
- Rare events, unfamiliar regions, and out-of-distribution earthquakes remain major sources of uncertainty.

## Contribute to this tutorial

Please refer to these [GitHub instructions](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project#about-forking) to open a pull request via the "fork and pull request" workflow. 

Pull requests will be reviewed by members of the Climate Change AI Tutorials team for relevance, accuracy, and conciseness.

## Climate Change AI Tutorials
Check out the [tutorials page](https://www.climatechange.ai/tutorials?) on our website for a full list of tutorials demonstrating how AI can be used to tackle problems related to climate change.

## License
Usage of this tutorial is subject to the MIT License.

## Cite

### Plain Text
Bhatnagar, T. (2026). Introduction to AI: Predicting Tsunami Alerts from Earthquake Observations [Tutorial]. In Climate Change AI Summer School. Climate Change AI. https://doi.org/10.5281/zenodo.21443710

### BibTeX

```
@misc{tarinibhatnagar2026tsunami,
  title={Introduction to AI: Predicting Tsunami Alerts from Earthquake Observations},
  author={Bhatnagar, Tarini},
  year={2026},
  organization={Climate Change AI},
  type={Tutorial},
  doi={https://doi.org/10.5281/zenodo.21443710},
  booktitle={Climate Change AI Summer School},
  howpublished={\url{https://github.com/climatechange-ai-tutorials/intro-ai-tsunami-alerts}}
}
```
