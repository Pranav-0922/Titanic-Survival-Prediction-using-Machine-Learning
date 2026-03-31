🚢 ****<ins>Titanic Survival Prediction using Machine Learning</ins>****

📌 Overview
    This project aims to predict passenger survival on the Titanic dataset using three machine learning models:
      * Logistic Regression
      * K-Nearest Neighbors (KNN)
      * Decision Tree Classifier

The dataset is taken from the Kaggle Titanic competition and includes features like age, gender, passenger class, fare, etc.
⚙️ Approach
   1. **Data Preprocessing**
      * Removed irrelevant columns: PassengerId, Name, Ticket, Cabin
      * Handled missing values:
      * Age → filled with median
      * Embarked → filled with mode
      * Encoded categorical variables:
      * Sex and Embarked using Label Encoding
        
   2. **Feature Selection**
       * Selected relevant features such as Pclass, Sex, Age, SibSp, Parch, Fare, Embarked

   3. **Train-Test Split**
      * Split dataset into 80% training and 20% testing

   4. **Model Training**
      * Logistic Regression
      * KNN
      * Decision Tree Classifier

   5. **Evaluation**
      * Compared models using accuracy score
      * Created a comparison table to identify the best-performing model

# ⚠️ **Difficulties Faced**

* Handling missing values in Age and Embarked columns
* Poor performance of KNN without feature scaling
* Overfitting in Decision Tree model
* Different feature scales affecting model performance

🛠️ **Resolutions**
     * Used median and mode to fill missing values
     * Applied StandardScaler for KNN and Logistic Regression
     * Tuned Decision Tree parameters (max_depth, min_samples_split)
     * Carefully selected relevant features for better generalization

##📊 **Results**

           | Model                 | Accuracy (approx) |
           | --------------------- | ----------------- |
           | Logistic Regression   | ~80%              |
           | KNN (with scaling)    | ~78–82%           |
           | Decision Tree (tuned) | ~82–85%           |

##👉 **Best Performing Model**
    * In my Scenerio,The Logistic Regression model achieved the highest accuracy of 80.4%, which is equal to KNN and slightly better than        Decision Tree.This indicates that the dataset has relatively simple and linearly separable patterns. Logistic Regression performs          well in such cases because it models the probability of survival using a linear decision boundary.
    * KNN also achieved the same accuracy due to proper feature scaling, which ensures accurate distance calculations.

##📚 **Learnings**
    * Importance of data preprocessing in machine learning
    * Handling missing values effectively
    * Feature scaling is crucial for distance-based models like KNN
    * Decision Trees can overfit if not properly tuned
    * Model comparison helps in selecting the best approach

##▶️ **How to Set Up and Run**
   1. Install Required Libraries
   ```bash
            pip install numpy pandas scikit-learn
   ```
   2. Download Dataset
     * Download Titanic dataset from Kaggle
     * Place `train.csv` in the project folder
   3. Run the Code
   ```bash
            python your_script_name.py
   ```

  4. Output
    * Accuracy comparison table will be displayed in the console
    * Best performing model will be identified

##📌 Conclusion:
This project demonstrates how different machine learning models perform on the same dataset and highlights the importance of preprocessing, feature scaling, and model tuning in achieving better results.
