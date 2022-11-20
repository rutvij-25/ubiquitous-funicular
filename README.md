# ubiquitous-funicular

### Key Highlights

1. Fine-tuned a BERT-base using transformers and PyTorch library
2. Run the notebook line by line  
3. For training I've used all datapoints from crypto_results and random 1000 datapoints from news,food,sports,art and music results
4. 10% of the data was used for testing, the distribution is as follows, train -> (4933 no + 2942 yes) and test -> (549 no + 327 yes)
5. The model was trained for 3 epochs using Kaggle GPUs
6. An accuracy of 93.0365 was achieved on test set (92.6 accuracy by taking 500 datapoints with distribution as, (3133 no + 2942 yes) and test -> (349 no + 327 yes)

### Problems encountered

- The model could not detect words like 'polygon','uniswap' and 'web3'.
- 'web3' was absent in the training set but 'polygon' and 'uniswap' were present (only a few instances)
- Possible Solutions
  1. Include term_abb and term_def files in the training set
  2. Train for more epochs
  3. Change model architecture and hyperparameter tuning
  4. Add more datapoints containing these words

