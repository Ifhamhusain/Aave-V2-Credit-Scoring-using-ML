#  Aave V2 Credit Scoring using Machine Learning

This project analyzes historical transaction data from the Aave V2 protocol and builds a machine learning model to predict credit risk scores of DeFi wallet addresses based on their behavior.

##  Features
- Parses JSON data from Aave V2 events.
- Extracts and engineers relevant features (like loan amounts, actions taken, etc.).
- Uses classification model to assign credit risk scores (Low, Medium, High).
- Outputs a labeled dataset and predictions for each wallet.
- Generates CSV reports for further analysis.

##  Technologies Used
- Python
- Pandas
- Scikit-learn
- Matplotlib & Seaborn (for visualizations)
- Jupyter Notebook

##  Dataset
- Raw input: Aave V2 event logs in JSON format.
- Transformed into structured DataFrame with wallet-level aggregations.

## Output
- Cleaned CSV with wallet addresses and their credit scores.
- Visual analysis of wallet behavior.
- Model accuracy and performance reports.

##  How to Run
1. Clone this repo:
    ```bash
    git clone https://github.com/your-username/aave-v2-credit-scoring.git
    cd aave-v2-credit-scoring
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Jupyter notebook or script:
    ```bash
    jupyter notebook
    ```
4. Check outputs in `output/` folder.


##  Author
- **Ifham Husain Zaidi**

