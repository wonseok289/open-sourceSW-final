# open-sourceSW-final
## (Configuration instructions)
  
  ## (1) (Used dataset)
  
  학습할 training dataset이 있는데 종양에 관한 데이터로, 4가지 glioma_tumor, meningioma_tumor, no_tumor, pituitary_tumor로 분류된다.
  
  train data에 과대적합되지 않도록, training dataset과 test dataset으로 split 했다.
  
  전처리:image data를 좌우반전시켜서 기존의 data에 append하여 수를 늘리었다.
  
  ## (2) (Used model)
  
  KNeighborsClassifier, DecisionTreeClassifier, DecisionTreeClassifier, DecisionTreeClassifier, ExtraTreesClassifier, SVC, SVC, SVC
  
  ## (3) (Used huperparameter)
  
  hyperparameter of KNeighborsClassifier:
  
  1. n_neighbors
  
    int, default=5

    Number of neighbors to use by default for kneighbors queries.
  
  2. p
    
    int, default=2
    
    Power parameter for the Minkowski metric. When p = 1, this is equivalent to using manhattan_distance (l1), and euclidean_distance (l2) for p = 2. For arbitrary p,       
    minkowski_distance (l_p) is used.
  
  hyperparameter of DecisionTreeClassifier:
  
  1. splitter
  
    {“best”, “random”}, default=”best”
 
    The strategy used to choose the split at each node. Supported strategies are “best” to choose the best split and “random” to choose the best random split.
  
  2. max_features
  
    int, float or {“auto”, “sqrt”, “log2”}, default=None

    The number of features to consider when looking for the best split
  
  3. random_state
  
  int, RandomState instance or None, default=None

  Controls the randomness of the estimator. The features are always randomly permuted at each split, even if splitter is set to "best". When max_features < n_features, 
  
  the algorithm will select max_features at random at each split before finding the best split among them. But the best found split may vary across different runs, 
  
  even if max_features=n_features. That is the case, if the improvement of the criterion is identical for several splits and one split has to be selected at random. To 
  
  obtain a deterministic behaviour during fitting, random_state has to be fixed to an integer.
  
  hyperparameter of SVC:
  
  1. C
  
  float, default=1.0

  Regularization parameter. The strength of the regularization is inversely proportional to C. Must be strictly positive. The penalty is a squared l2 penalty.
  
  2. kernel
  
  {‘linear’, ‘poly’, ‘rbf’, ‘sigmoid’, ‘precomputed’} or callable, default=’rbf’

  Specifies the kernel type to be used in the algorithm. If none is given, ‘rbf’ will be used. If a callable is given it is used to pre-compute the kernel matrix from 
  
  data matrices; that matrix should be an array of shape
  
  3. gamma
  
  {‘scale’, ‘auto’} or float, default=’scale’

  Kernel coefficient for ‘rbf’, ‘poly’ and ‘sigmoid’.
  
  4. probability
  
  bool, default=False

  Whether to enable probability estimates. This must be enabled prior to calling fit, will slow down that method as it internally uses 5-fold cross-validation, and 
  
  predict_proba may be inconsistent with predict. Read more in the User Guide.
  
  5. verbose
  
  bool, default=False

  Enable verbose output. Note that this setting takes advantage of a per-process runtime setting in libsvm that, if enabled, may not work properly in a multithreaded     
  context.
  
  6. random_state
  
  int, RandomState instance or None, default=None

  Controls the pseudo random number generation for shuffling the data for probability estimates. Ignored when probability is False. Pass an int for reproducible output 
  
  across multiple function calls.
  
  hyperparameter of ExtraTreesClassifier:
  
  1. n_estimators
  
  int, default=100
  
  The number of trees in the forest.
  
  2. criterion
  
  {“gini”, “entropy”, “log_loss”}, default=”gini”

  The function to measure the quality of a split. Supported criteria are “gini” for the Gini impurity and “log_loss” and “entropy” both for the Shannon information 
  
  gain, see Mathematical formulation. Note: This parameter is tree-specific.
  
  3. random_state
  
  int, RandomState instance or None, default=None

  Controls 3 sources of randomness:

  the bootstrapping of the samples used when building trees (if bootstrap=True)

  the sampling of the features to consider when looking for the best split at each node (if max_features < n_features)

  the draw of the splits for each of the max_features
  
## (Operating instructions) 
  
  Open file, and run all codes in order.
  
  Operate ipynb file with pickle file.

## (Copyright and licensing information) 
  
  MIT license

## (Contact information for the distributor or author) 
  
  Name: Wonseok Choi
  
  Email: jsandjk@cau.ac.kr
  
  Student id: 20224258
