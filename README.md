# ESM2-Ubiquitination Prediction
## Introduction
### Author Contact Information:
Author 1: Junhao Liu, Email: 895232226@qq.com

Author 2: Zeyu Luo, Email: 1024226968@qq.com, https://orcid.org/0000-0001-6650-9975

Author 3: Rui Wang, Email: 2219312248@qq.com
## Data available
### Inference Test Data

To evaluate the performance of the EUP models, we have prepared a independent test dataset:

- **[ESM2_3B_2560](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Inference_test_data/ESM2_3B_2560)**: This dataset contains raw input data without any preprocessing, suitable for testing all models.

## EUP Environment Setup
You can follow the instructions provided at [ESM2-Ubiquitination-Prediction/Instruction/EUP Online Analysis Guide.md](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Instruction) to use the [web server](https://eup.aibtit.com) for online predictions.
## Models

In this project, we have constructed four deep learning models for the ubiquitination site prediction task, specifically including:

- **[DNNLinerModel](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Model/DNNLinerModel)**: A linear model based on fully connected layers (Dense Layer). This model directly learns the prediction rules of ubiquitination sites from raw input data.
- **[ResDNNModel](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Model/ResDNNModel)**: A deep neural network model that introduces residual blocks (Residual Block). Through the residual learning mechanism, this model can effectively alleviate the problem of vanishing gradients, enhancing the model's ability to learn from deep structures.
- **[cVAE_DNNLinerModel](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Model/cVAE_DNNLinearModel)**: A conditional VAE model combining a Residual Variational Autoencoder (ResVAE) with DNN_LinerModel as the classification head. This model framework is trained with both reconstruction and classification objectives. During prediction, the features are directly input into the model framework, and ubiquitination site prediction is performed in the classification head DNN_LinerModel.
- **[cVAE_ResDNNModel](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/tree/main/Model/cVAE_ResDNNModel)**: A conditional VAE model combining a Residual Variational Autoencoder (ResVAE) with ResDNNModel as the classification head. This model framework is trained with both reconstruction and classification objectives. During prediction, the features are directly input into the model framework, and ubiquitination site prediction is performed in the classification head ResDNNModel.
- **ESMc support**: Please see this [document](https://github.com/EUP-laboratory/ESM2-Ubiquitination-Prediction/blob/main/update_new.md) for detail. 

## Reference


## Citation


## Acknowledgments

We are acknowledge the contributions of the open-source community and the developers of the Python libraries used in this study.

## Related Works
If you are interested in feature extraction and model interpretation for large language models, you may find our previous work helpful:
- **Interpretable feature extraction and dimensionality reduction in ESM2 for protein localization prediction**: [GitHub Repository](https://github.com/yujuan-zhang/feature-representation-for-LLMs)
