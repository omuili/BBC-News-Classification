# BBC News Classification Project

## Overview
This project classifies BBC News articles into five categories (sport, tech, business, entertainment, politics) using both unsupervised matrix factorization techniques and supervised learning methods. The project focuses on comparing these approaches, especially examining how they perform with varying amounts of labeled data.

## Dataset
- **Training data**: 1490 labeled news articles
- **Testing data**: 735 news articles for prediction
- **Categories**: sport, tech, business, entertainment, politics
- **Evaluation metric**: Accuracy

## Key Features
- Comprehensive exploratory data analysis of news articles
- Text preprocessing and feature extraction using TF-IDF
- Unsupervised learning through matrix factorization (NMF, LDA, SVD)
- Supervised learning models for comparison (Random Forest, Naive Bayes)
- Analysis of model performance with varying amounts of training data
- Topic visualization and interpretation

## Project Structure
```
├── notebooks/
│   └── BBC_News_Classification.ipynb    
├── data/
│   ├── BBC News Train.csv              
│   ├── BBC News Test.csv               
│   └── BBC News Sample Solution.csv   
├── submissions/                       
├── visualizations/                    
├── README.md                         
└── requirements.txt               
```

## Installation and Setup
1. Clone this repository
2. Install required packages:
   ```
   pip install -r requirements.txt
   ```
3. Place the dataset files in the `data/` directory
4. Run the Jupyter notebook

## Methods
### Unsupervised Learning
- **Feature Extraction**: TF-IDF vectorization
- **Matrix Factorization**: 
  - Non-negative Matrix Factorization (NMF)
  - Latent Dirichlet Allocation (LDA)
  - Truncated Singular Value Decomposition (SVD)
- **Topic Discovery**: Extracting latent topics from news articles
- **Classification**: Assigning categories based on topic distributions

### Supervised Learning
- **Feature Extraction**: TF-IDF vectorization
- **Models**: 
  - Random Forest Classifier
  - Multinomial Naive Bayes
- **Training**: Various proportions of the labeled data (10%, 25%, 50%, 75%, 100%)

## Results
The project compares:
- Performance of different matrix factorization methods
- Effect of varying the number of latent topics/components
- Supervised vs. unsupervised approaches
- Data efficiency and overfitting tendencies

## Submission Format
The submission file contains two columns:
- `ArticleId`: ID from the test file
- `Category`: Predicted category (sport, tech, business, entertainment, or politics)

## Dependencies
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- nltk
- wordcloud

## References
- Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent Dirichlet allocation. *Journal of Machine Learning Research, 3*, 993-1022.
- Lee, D. D., & Seung, H. S. (1999). Learning the parts of objects by non-negative matrix factorization. *Nature, 401(6755)*, 788-791.
- Deerwester, S., Dumais, S. T., Furnas, G. W., Landauer, T. K., & Harshman, R. (1990). Indexing by latent semantic analysis. *Journal of the American Society for Information Science, 41(6)*, 391-407.

## License
MIT
