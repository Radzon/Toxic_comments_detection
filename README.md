# Text Classification Model for Russian Comments

## Project Overview
This project aims to develop and evaluate text classification models for identifying Russian comments. The project has three primary tasks:
1. Develop a model to accurately classify Russian comments.
2. Ensure that the model achieves a Precision score of at least 95%.
3. Maximize the Recall score for the classification task.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training and Evaluation](#training-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Dataset
The dataset consists of labeled Russian comments. Each comment is labeled as either `__label__NORMAL` or another category, indicating whether the comment is normal or not. The dataset is provided in a text file with each line containing a label and a comment.

### Data Preprocessing
1. The data is read from a file and split into comments and labels.
2. The data is balanced by downsampling the majority class to match the minority class size.
3. The text data is tokenized and padded to ensure uniform input length for the model.

## Model Architecture
The model is built using TensorFlow and Keras, utilizing the following architecture:
- **Embedding Layer**: Converts text data into dense vector representations.
- **Bidirectional LSTM Layers**: Captures contextual information from both directions in the text.
- **Dropout Layers**: Regularizes the model to prevent overfitting.
- **Dense Layer**: Outputs the classification results with a sigmoid activation function.

## Training and Evaluation
The model is trained using the Adam optimizer and binary cross-entropy loss function. Early stopping and model checkpointing are used to optimize training.

### Training Process
- The dataset is split into training and testing sets.
- The model is trained for a maximum of 20 epochs with a batch size of 32.
- Early stopping is applied with a patience of 3 epochs based on validation accuracy.

### Evaluation Metrics
- **Precision**: Ensuring at least 95% precision.
- **Recall**: Maximizing the recall score.

## Results
The model achieves the following performance on the test set:
- **Precision**: 95%
- **Recall**: Maximized by the model's architecture and training process.

## Contributing
We welcome contributions to improve the model and the project. Please fork the repository and submit pull requests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links
- [Dataset on Kaggle](https://www.kaggle.com/datasets/alexandersemiletov/toxic-russian-comments?select=dataset.txt)
- [Author's idea video on YouTube](https://www.youtube.com/watch?v=RVUpCdVhF60&t=1141s)
