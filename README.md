# charity-funding-predictor
Using Alphabet Soup donations data to predict whether recipients will be successful.

## Report

### Overview
The purpose of this project is to analyze past data from Alphabet Soup’s donation history in order to predict the value of future predictions. More specifically, we have data such as asking amount, industry or sector affiliation, organization type, and ask amount. The data set includes whether or not the organization made successful use of the donation or not. The method utilized to attempt to solve this problem was preprocessing of data and the creation of a neural network with a few versions featuring tweaks to hyperparameters.

### Results

#### Data Preprocessing
- Target Variable
  - Whether the Organization was Successful
- Feature Variables
  - Application Type
  - Affiliation
  - Classification
  - Use Case
  - Organization
  - Status
  - Income Amount
  - Special Considerations
  - Ask Amount
- Removed Variables
  - Name
  - EIN

#### Model Details
- The original neural network model used two hidden layers with 16 neurons each. The ReLU activation function was used for the hidden layers and the sigmoid function was used for the output layer. All parameters were selected as relatively safe and proven specifications. 
- The target accuracy of this model was 72.82%, which was right below the goal accuracy (75%).
- While optimizing, a third hidden layer was added first (72.82% accuracy). The next change was lowering the number of epochs from 100 to 50 (73.18%). Finally, the Use Case feature was removed to attempt to reduce data complexity, and 72.98% accuracy was achieved with this iteration of the model. These changes only made minor impacts on the overall accuracy, but the model with three hidden layers and 50 epochs was the most effective.

### Summary
The model created to predict success of organizations that receive donations from Alphabet Soup proved to be semi-successful. All iterations of the neural network model performed about 2% below our targeted accuracy, which means further preprocessing of data and tweaking hyperparameters may prove to raise the accuracy above 75%. If further modeling were to be performed, Random Forest Classifier models might prove effective, as each feature will be properly weighted and both the categorical and continuous data will be well accounted for. Another option to explore may be the K-Nearest Neighbors algorithm, as much of the data shares classifications and will likely form clusters that this model could predict if there is a true pattern in success rates.
