<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->

<a id="readme-top"></a>

  <h3 align="center">Causal Model for Bias Detection and Mitigation for CNN</h3>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <!-- <li><a href="#roadmap">Roadmap</a></li> -->
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <!-- <li><a href="#acknowledgments">Acknowledgments</a></li> -->
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

This project aims to detect and mitigate bias in Convolutional Neural Networks (CNNs) using causal models. It utilizes the FairFace dataset and applies data preparation and model training to identify biases and implement mitigation strategies.

It is **strongly recommended** to run this project using Google Colab Pro+ due to the high computing power required for dataset preparation.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- [Python](https://www.python.org/)
- [R](https://www.r-project.org/)
- [Google Colab](https://colab.research.google.com/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

To get a local copy up and running, follow these steps.

### Prerequisites
#### Download data from HuggingFace FariFace Dataset. 
Link: https://huggingface.co/datasets/HuggingFaceM4/FairFace
Using the following code block:
```
from datasets import load_dataset

ds = load_dataset("HuggingFaceM4/FairFace", "0.25")
```
- Google Colab Pro+ account (strongly recommended)
- Python (for running data preparation)
- R (for running the causal model)
- FairFace Dataset (`archive.zip` located in the `Data` folder)

### Installation

1. **Unzip the FairFace Dataset**

   Unzip the `archive.zip` file located in the `Data` folder. The unzipped content `FairFace` folder should contain:
   ```
   FairFace/
   ├── train/
   ├── val/
   ├── train_labels.csv
   └── val_labels.csv
   ```
3. **Run Data Preparation**

Run the `Data_Preparation.ipynb` notebook (written in Python). This notebook processes the dataset and outputs several CSV files, which can be found in the `Output` folder:

- `test_data_100_with_emotions.csv`: CSV to test if the DeepFace model is labeling the FairFace dataset correctly.
- `full_data_with_emotions.csv`: CSV containing the fully emotion-labeled dataset (with only domain emotions).
- `test_predictions.csv`: CSV containing probabilities for each emotion class. This is used for the causal model.

3. **Run Causal Model**

Using the `test_predictions.csv` file, run the `causal_model.ipynb` notebook (written in R). This will output the following CSV file:

- `binarized_test_predicted_data.csv`

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

This project can be used to understand and mitigate biases present in CNN models, especially those related to facial recognition and emotion detection. By following the steps above, you can replicate the study and explore the effects of bias in machine learning models.

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!


## Contact

Your Name - [@Roy-Byun](https://github.com/Roy-Byun) - roybyun722@gmail.com

Project Link: [https://github.com/Roy-Byun/IDC2808-Casual-Model-for-Bias-Detection-and-Mitigation-for-CNN](https://github.com/Roy-Byun/IDC2808-Casual-Model-for-Bias-Detection-and-Mitigation-for-CNN)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
<!--
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p>
-->

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
