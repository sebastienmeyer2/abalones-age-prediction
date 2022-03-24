# Abalones Age Prediction

Abalones are one type of reef-dwelling marine snails. It is difficult to tell the ages of abalones because their shellsizes not only depend on how old they are, but also depend on the availability of food. The study of age is usually by obtaining a stained sample of the shell and looking at the number of rings through a microscope. We are interested in using some of abalones physical measurements, especially the height measurement to predict their ages. Biologists believe that a simple linear regression model with normal error assumption is appropriate to describe the relationship between the height of abalones and their ages. In particular, that a larger height is associated with an older age.

The dataset and its description are available at https://archive.ics.uci.edu/ml/datasets/Abalone.

This team is: Sébastien Meyer, Ziru Niu and 2 other students.

Please refer to the following sections for more information about the package:

1. [Our results](#our-results)
2. [Installation](#installation-instructions)
3. [Description](#package-description)

## Our results

A brief summary of our results is available in our report under *report/abalone_report.pdf*. Below, we only give a summary table of the MSE of different models.

| Method                    | MSE    | Features                                                 |
| ------------------------- | ------ | -------------------------------------------------------- |
| Kernel estimator          | 14.100 | Height + grid search                                     |
| Simple linear model       | 6.902  | Height and Height<sup>2</sup> + *log* dependent variable |
| XGBoost                   | 5.000  | Selected features + grid search                          |
| Random Forest             | 4.966  | Selected features + grid search                          |
| GLMNet                    | 4.824  | Selected features                                        |
| Multivariate linear model | 4.759  | Selected features + *log* dependent variable             |

## Installation instructions

Our package has been tested under R version 4.1.2 on Linux. We recommend you to set up the following working environment: R, [VSCodium](https://vscodium.com/) and [radian](https://github.com/randy3k/radian). All the necessary packages are mentioned in the *abalone_project.Rmd* file. You will also need the *knitr* library to knit the file.

## Package description

Below, we give a brief tree view of our package.

    .
    ├── README.md
    ├── report  # contains a brief report and figures
    ├── abalone_data.csv
    ├── abalone_project.html  # knitted code
    └── abalone_project.Rmd  # contains all our code

