# Hand vs Foot Motor Execution Classification with Deep Learning

This repository contains the code and analysis for a project focused on classifying EEG (Electroencephalogram) signals to distinguish between **hand** and **foot** motor execution. This project explores and compares the effectiveness of deep learning architecture: **Convolutional Neural Networks (CNN)**.

The primary goal is to build a robust classifier for Brain-Computer Interface (BCI) applications, such as assistive technology or motor rehabilitation.

## Table of Contents

- [About The Project](#-about-the-project)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Installation](#-installation)
- [Usage](#-usage)
- [Results](#-results)

## About The Project

This project investigates the feasibility of decoding motor execution (ME) tasks from non-invasive EEG signals:
* **CNN**: To automatically learn spatio-temporal features directly from the raw or preprocessed EEG data.

## Dataset
This project uses the **EEG Motor Movement/Imagery Dataset (EEGMMIDB)**, a well-known dataset from PhysioNet, which is standardized for BCI research.

The data is loaded and accessed using the MNE-Python library, specifically via the `mne.datasets.eegbci.load_data` function.

* **Source:** [PhysioNet BCI 2000 / EEGMMIDB](https://physionet.org/content/eegmmidb/1.0.0/)
* **Subjects:** 109 subjects are available (the loader function can download them individually).
* **Channels:** 64 EEG channels (recorded using the BCI2000 system).
* **Sampling Rate:** 160 Hz.
* **Task:** This project focuses on **Motor Execution (ME)**.
* **Specific Runs:** We use **runs 5, 9, and 13** from the dataset, which correspond to the motor execution tasks for:
    * **T1: Both fists**
    * **T2: Both feet**
* **Data Access:** The dataset is downloaded automatically by the MNE library when the function is called. No manual download is required. See the MNE documentation for [mne.datasets.eegbci.load_data](https://mne.tools/stable/generated/mne.datasets.eegbci.load_data.html) for more details.
