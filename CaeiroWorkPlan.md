# EDA of Detected Human Poses in Election Debates

This repository contains code and documentation for the exploratory data analysis (EDA) of detected human poses during the election debates in Portugal.

## Overview

In the weeks leading up to the election day in March 2024, eight major political parties participated in one-on-one debates broadcasted on three Portuguese TV channels. For each frame of these debates, information was extracted using various detectors, including:

- Detected objects
- Detected human poses
- Detected faces and emotions
- Image embedding vectors

This README specifically focuses on the EDA related to the detected human poses.

## Dataset Description

The dataset consists of:

- 3D coordinates of 33 keypoints for each detected human pose
- Probability of each pose being visible and present
- Other metadata related to the poses

## EDA Tasks

The following exploratory data analysis tasks were performed:

1. **Distribution of Pose Confidence**: Summary statistics and visualization of the probability of poses being visible and present.

2. **Pose Keypoints Analysis**: Summary statistics and visualization of the distribution of individual keypoints across all detected poses.

3. **Pose Variability**: Measurement and visualization of pose variability or consistency across frames.

4. **Pose Relationships**: Exploration of relationships between different keypoints within a pose.

5. **Pose Clustering**: Clustering analysis to group similar poses together based on keypoint positions.

6. **Pose Dynamics**: Investigation of pose dynamics over time, including velocity and acceleration.

7. **Pose Comparison Across Parties/Debates**: Comparison of poses detected during debates for different parties or across different debate sessions.

## Files

- `pose_eda.ipynb`: Jupyter notebook containing the code for the EDA tasks.
- `data.pickle`: Pickle file containing the raw data extracted from the debate videos.

## Requirements

- Python 3.x
- Jupyter Notebook
- pandas, numpy, matplotlib, seaborn (Python libraries)

## Usage

1. Clone the repository:

