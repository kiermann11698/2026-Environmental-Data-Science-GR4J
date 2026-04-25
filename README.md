# Evaluating GR4J Parameter Transferability Across U.S. Catchments
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kiermann11698/2026-Environmental-Data-Science-GR4J/main)

This project uses hydrologic modeling and machine learning to evaluate how GR4J rainfall-runoff model parameters can be regionalized across U.S. catchments. The goal is to improve streamflow prediction in ungauged or poorly gauged watersheds by transferring calibrated model parameters using catchment descriptors, spatial proximity, and machine learning methods.

## Data Sources

- Daily precipitation, evapotranspiration, and observed runoff data for U.S. catchments
- Catchment descriptor data including climate, hydrologic signatures, topography, soil, geology, and land-cover variables
- Latitude and longitude data for spatial proximity analysis
- Calibrated GR4J parameter outputs for X1, X2, X3, and X4
- Model performance metrics including calibrated and validated Nash-Sutcliffe Efficiency (NSE)

## Methods

- Automated GR4J rainfall-runoff model calibration
- Parameter optimization using SPOTPY
- Shuffled Complex Evolution at the University of Arizona (SCE-UA) algorithm
- Calibration period: 1980–2004
- Validation period: 2005–2014
- Model evaluation using Nash-Sutcliffe Efficiency (NSE)
- Regionalization using a 70% training and 30% hidden holdout testing framework
- Descriptor-based and spatial parameter transfer approaches

## Machine Learning and Regionalization

- Linear Regression
- Random Forest
- Support Vector Regression (SVR)
- Descriptor-based K-Nearest Neighbor (KNN)
- Spatial proximity parameter transfer
- Model evaluation using R² values for predicted versus calibrated GR4J parameters
- Comparison of parameter transferability across X1, X2, X3, and X4

## Findings

- Random Forest produced the strongest overall regionalization performance, especially for X1, X2, and X4.
- Support Vector Regression also performed well, particularly for X1 and X2.
- Linear Regression showed weaker overall performance, suggesting that many parameter-descriptor relationships are nonlinear.
- X1 was the most predictable GR4J parameter across methods.
- X4 was the most difficult parameter to regionalize, with consistently low R² values.
- Descriptor-based KNN was competitive for X3 and X4.
- Spatial proximity alone performed poorly for most parameters, suggesting that geographic closeness is less useful than descriptor similarity.
- NSE values showed clear spatial variability across the United States, with stronger model performance in some eastern, southeastern, and West Coast catchments.

## Contents

- `Final_Report/` – Final written report and project documentation
- `Presentation/` – Final presentation materials
- `data/` – Input data, catchment descriptors, and processed datasets
- `notebooks/` – GR4J calibration, validation, regionalization, and visualization notebooks
- `README.md` – This file

## Team

This project was completed as part of EGN 4930 – Special Topics: Environmental Data Science at Florida Gulf Coast University.

Team members: Samuel Cabrera, Yelen Gonzalez, Jonathan Guerrero, and Kieran Mannering

Instructor: Dr. Ahmed Elshall

## About

This repository contains code, data, visualizations, and documentation for evaluating GR4J rainfall-runoff model parameter transferability across U.S. catchments. The project combines automated hydrologic model calibration with machine learning-based regionalization methods to support streamflow prediction in ungauged watersheds.
