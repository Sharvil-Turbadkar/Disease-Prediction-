# Disease-Prediction-
Predicting whether a patient has a disease given his biodata
Preprocessed data using EDA
Winsorized, Scaled and Normalized data followed by using One-hot Encoding for converting numerical variables to categorical variables 
Applied Ensemble Learning models that aggregate multiple tree-based models 
Used Sigmoidal function as an activation function to squash values between 0 and 1       
Used Leaky ReLU as ReLU is linear (identity) for all positive values, and zero for all negative values. This means that:
It’s cheap to compute as there is no complicated math. The model can, therefore, take less time to train or run.
It converges faster. Linearity means that the slope doesn’t plateau, or “saturate,” when x gets large. It doesn’t have the vanishing gradient problem suffered by other activation functions like sigmoid or tanh.
It’s sparsely activated. Since ReLU is zero for all negative inputs, it’s likely for any given unit to not activate at all. This is often desirable (see below).
Used SVM as it draws a Linear hyperplane to differentiate between positive and negative target variables. Both ANN-0 when used with a sigmoid activation function and logistic regression use binary cross-entropy loss to differentiate between the target variables
However in ANN-0 the weights are updated as back-propagation is used. Back-propagation is an iterative method. We start with some set of values for our model parameters (weights and biases), and improve them slowly.
Partial computations of the gradient from one layer are reused in the computation of the gradient for the previous layer. This backward flow of the error information allows for efficient computation of the gradient at each layer thus reducing the cost
This is the reason we get lower costs and thus higher accuracies for ANN-0 than for logistic regression

Feature Importance 

Feature selection is a process where you automatically select those features in your data that contribute 
most to the prediction variable or output in which you are interested. Three benefits of performing feature selection 
before modeling your data are:

Testing Accuracies	 	 	 	 	 
NBC	    KNN		  SVM Linear SVM RBF	RF	      GBM
61.5127	71.0008	72.38052	72.46551	72.55549	72.77045

Testing Accuracies:-	 	 	 	 
Decision Trees	 LogisticRegression	ANN0	    ANN1	    ANN2
71.0058	         65.64187	          66.33173	65.57688	68.78624
