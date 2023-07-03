# Bicing-Avaiability-Prediction

## Introduction

Repository created to organize the code regarding the Bicing Avaiability Prediction Project for the Data Science and Machine Learning course.
The member of the group are:

👤 Guillermo López
👤 Berta Nieto
👤 Francesc Polls
👤 David Serrano

The user that has been used to make the submissions is:
Francesc Polls (https://www.kaggle.com/francescpolls)

## Objective

- To explore data in a 'real world' setting.
- To identify relevant insights and patterns.
- To develop a competitive model.

## Project

The purpose of this project is to develop a machine learning program that can accurately predict the occupancy levels of various stations in Barcelona. The project involves a series of steps, starting with data collection and preprocessing.

In the data collection phase, we download the data on a monthly basis and calculate the hourly averages for each station. Additionally, we incorporate information about rainfall (detected by the Fabra Observatory) and strong winds (exceeding 20m/s) for each day. We also include other relevant information such as the day of the year, month, hour, and day of the week. Lines with missing data or other issues are discarded to ensure data quality.

Next, we move on to the analysis programs. Here, we prepare the dataset for making predictions. To train the models, we only utilize the data from 2021 and 2022 to avoid any biases introduced by the COVID-19 pandemic. We also add information about holidays (weekends or August) and the season of the year. Similar to the data collection phase, lines with missing data or other issues are eliminated.

We then proceed with the implementation of a neural network. Initially, the network was too small, and the program struggled to classify the data, resulting in consistently predicting the average station occupancy. To address this, we increased the number of layers and neurons in the neural network, including dense layers and layers to eliminate outliers. This modification improved the results, although an acceptable outcome was still out of reach. To further enhance the performance, we introduced a principal component analysis and incorporated new variables representing the occupancy percentages of previous hours.

In addition to the neural network, we explored the utilization of LightGBM, a program that employs the same data and values as the neural network but offers faster processing. LightGBM also allows for the designation of categorical variables, which proved beneficial since station IDs are categorical. This improvement, combined with the inclusion of occupancy percentages from previous hours, significantly enhanced the accuracy of the predictions.

Moving forward, there are several areas for potential improvement. First, we aim to incorporate more information about the stations, such as their locations in Barcelona, to group them by zones and utilize station embeddings for categorical treatment in the neural network. This is crucial for enabling the network to identify patterns based on geographic areas. Additionally, we plan to incorporate more information from meteorological stations in different zones. Lastly, we intend to include data on university calendars, annual holidays, and FC Barcelona matches to further refine the predictions. These enhancements will contribute to the overall accuracy and usefulness of the machine learning program. 