# Spark Home Sales Analysis

This project utilizes Apache Spark for analyzing a dataset containing information about home sales. It includes various Spark SQL queries for data exploration and provides insights into the average prices of homes based on different criteria.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Running the Code](#running-the-code)
- [Usage](#usage)
  - [1. Data Loading](#1-data-loading)
  - [2. Temporary Table Creation](#2-temporary-table-creation)
  - [3. Queries](#3-queries)
  - [4. Caching](#4-caching)
  - [5. Parquet Data](#5-parquet-data)
  - [6. Uncaching](#6-uncaching)
- [Acknowledgements](#acknowledgements)

## Overview

This Spark project aims to analyze home sales data using Spark SQL queries. It provides insights into the average prices of homes based on various criteria, such as the number of bedrooms, bathrooms, floors, and square footage.

## Prerequisites

Before running the code, ensure you have the following prerequisites:

- Apache Spark installed
- Python with PySpark

## Getting Started

### Installation

Install Apache Spark and set up PySpark on your machine.

### Running the Code

Clone this repository and run the Spark script using PySpark.

## Usage

### 1. Data Loading

The project reads data from an AWS S3 bucket into a Spark DataFrame.

### 2. Temporary Table Creation

A temporary view named 'home_sales' is created from the DataFrame.

### 3. Queries

Several Spark SQL queries are executed to analyze the data, including:

- Average price for a four-bedroom house sold in each year.
- Average price of a home with three bedrooms and three bathrooms.
- Average price of a home with specific criteria (bedrooms, bathrooms, floors, and square footage) for each year built.
- View rating for the average price of homes with prices greater than or equal to $350,000.

### 4. Caching

The 'home_sales' table is cached for improved performance.

### 5. Parquet Data

The script partitions the home sales dataset by the "date_built" field and reads the formatted parquet data.

### 6. Uncaching

The 'home_sales' table is uncached when necessary.

## Acknowledgements

- [Apache Spark](https://spark.apache.org/) 
- [PySpark](https://spark.apache.org/docs/latest/api/python/index.html) 

Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only - University of Toronto. 
