---
title: Example Jupyter Notebooks (v1)
titleSuffix: Azure Machine Learning
description: Learn how to find and use the Juypter Notebooks designed to help you explore the SDK (v1) and serve as models for your own machine learning projects.
services: machine-learning
ms.service: machine-learning
ms.subservice: core
ms.topic: sample

author: sdgilley
ms.author: sgilley
ms.reviewer: sgilley
ms.date: 12/27/2021
ms.custom: seodec18
#Customer intent: As a professional data scientist, I find and run example Jupyter Notebooks for Azure Machine Learning.
---

# Explore Azure Machine Learning with Jupyter Notebooks (v1)

[!INCLUDE [sdk v1](../../../includes/machine-learning-sdk-v1.md)]
> [!div class="op_single_selector" title1="Select the Azure Machine Learning version you are using:"]
> * [v1](<samples-notebooks-v1.md>)
> * [v2 (preview)](../samples-notebooks.md)

The [Azure Machine Learning Notebooks repository](https://github.com/azure/machinelearningnotebooks) includes Azure Machine Learning Python SDK (v1) samples. These Jupyter notebooks are designed to help you explore the SDK and serve as models for your own machine learning projects.  In this repository, you'll find tutorial notebooks in the **tutorials** folder and feature-specific notebooks in the **how-to-use-azureml** folder.

This article shows you how to access the repositories from the following environments:

- Azure Machine Learning compute instance
- Bring your own notebook server
- Data Science Virtual Machine


## Option 1: Access on Azure Machine Learning compute instance (recommended)

The easiest way to get started with the samples is to complete the [Quickstart: Get started with Azure Machine Learning](../quickstart-create-resources.md). Once completed, you'll have a dedicated notebook server pre-loaded with the SDK and the Azure Machine Learning Notebooks repository. No downloads or installation necessary.

## Option 2: Access on your own notebook server

If you'd like to bring your own notebook server for local development, follow these steps on your computer.

[!INCLUDE [aml-your-server](../../../includes/aml-your-server.md)]

These instructions install the base SDK packages necessary for the quickstart and tutorial notebooks. Other sample notebooks may require you to install extra components. For more information, see [Install the Azure Machine Learning SDK for Python](/python/api/overview/azure/ml/install).

## Option 3: Access on a DSVM

The Data Science Virtual Machine (DSVM) is a customized VM image built specifically for doing data science. If you [create a DSVM](how-to-configure-environment-v1.md), the SDK and notebook server are installed and configured for you. However, you'll still need to create a workspace and clone the sample repository.

[!INCLUDE [aml-dsvm-server](../../../includes/aml-dsvm-server.md)]

## Next steps

Explore the [MachineLearningNotebooks](https://github.com/Azure/MachineLearningNotebooks) repository to discover what Azure Machine Learning can do.

For more GitHub sample projects and examples, see these repos:
+ [Microsoft/MLOps](https://github.com/Microsoft/MLOps)
+ [Microsoft/MLOpsPython](https://github.com/microsoft/MLOpsPython)

