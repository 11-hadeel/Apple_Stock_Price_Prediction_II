# Apple Stock Price Prediction Part II
## Sequence Modeling with Transformer-Based Architectures

This repository contains the second part of our group project, focusing on building and comparing different sequence modeling architectures for time-series forecasting. These include:

1. Vanilla Transformer
2. Autoformer
3. XFormer
4. Reformer
5. Custom Transformer Model

The models are implemented using PyTorch and aim to showcase the differences in architecture and performance.

#### Directory Descriptions

- **`data/`**: Contains raw and processed datasets.
- **`models/`**: Implementation of the different architectures.
- **`results/`**: Plots of the model performance.

### Models Overview

### Vanilla Transformer
- Positional encoding layer to capture sequence order.
- Multi-head attention, feed-forward layers, dropout, and layer normalization.
- Optimized for time-series forecasting tasks.

#### Autoformer
- Captures temporal patterns compactly.
- Efficient for sequences of varying lengths.
- Optimized for financial forecasting.

#### XFormer
- Combines input projection, a Transformer encoder, and a final linear layer.
- Configurable layers and attention heads.
- Suitable for time-series forecasting and sequential pattern analysis.

#### Reformer
- Memory-efficient architecture for long sequences.
- Reduced attention complexity.
- Handles larger datasets effectively.

#### Custom Transformer Model
- Simplified architecture without positional encodings.
- Designed for smaller datasets.
- Combines multi-head attention and feed-forward layers for temporal dependencies.

## Performance Evaluation  

### Metrics  
Models were evaluated using:  
- **Mean Squared Error (MSE)**  
- **Mean Absolute Error (MAE)**  
- **Root Mean Squared Error (RMSE)**  
- **Mean Absolute Percentage Error (MAPE)**  
- **R² (R-squared)**  

### Training and Inference Times  
- **Reformer**: Fastest inference, efficient for long sequences.  
- **Vanilla Transformer**: Longest training time due to high complexity.  

### Model Comparison  
| Model              | MSE    | R²     | Notes                                   |  
|--------------------|--------|--------|-----------------------------------------|  
| **Reformer**       | 0.0023 | 0.9890 | Best overall: accuracy + efficiency.    |  
| **Vanilla**        | 0.0013 | 0.9524 | Strong general-purpose model.           |  
| **Autoformer**     | 0.0019 | 0.9741 | High MAPE in specific scenarios.        |  
| **XTransformer**   | 0.0038 | 0.8634 | Balanced for medium-complexity tasks.   |  
| **Custom**         | 0.0037 | 0.9488 | Ideal for small datasets, efficient.    |  

### Conclusion  
The **Reformer** outperformed other models with superior accuracy and efficiency. The **Vanilla Transformer** and **Autoformer** delivered high accuracy but at higher resource costs. The **XTransformer** and **Custom Transformer** provided balanced performance for specific use cases. Model selection depends on dataset size and task complexity. In our **Reformer** is was the most suitable.



