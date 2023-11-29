# Temporal GNN Predictions to Aid Investment Decisions using Company Relationship Graphs

CSC 591/791, Fall 2023, NC State  
ML with Graphs, Professor: Xiaorui Liu  
Team: Levi Kennedy, Ayush Pathak, Michael Dacanay


## Description

Defining a graph structure with companies as nodes, and using a Temporal GCN to train a model to predict stock price and earnings outcome.

Node features: [price, volume, month, year]
Edge can be either unweighted (set to 1) or weighted.

Edge definitions:  

1. Define edge between each pair of companies where edge weight is the cosine similarity of (NLP) vector embedding of company description and sector.
2. Define edge between 2 nodes(companies) if a US Congress politician invests in both companies. Edge weight is higher for each additional politician that invests in both companies. The edge weights are then normalized to [0,1].
3. Define edge between 2 nodes(companies) depending on business relationships dataset.


For more detail, see [presentation](https://docs.google.com/presentation/d/1kI4A_ki5VXhGKz3LbQJMFg1aCfbJSltj-xa66N8P1ns/edit#slide=id.g29d67d3b3b6_0_98).


## Environment setup

**Step 1**: Activate virtual environment and install dependencies  
`pipenv shell`

OR 

```
python -m venv venv
source ./venv/Scripts/activate
pip install -r requirements.txt

# to exit virtual environment
deactivate
```

**Step 2**: Open Jupyter Lab  
`jupyter lab`: this opens up a Jupyter notebook environment in the browser

