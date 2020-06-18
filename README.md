# Association_rule_learning :

Association rule learning is a rule-based machine learning method for discovering interesting relations between variables in large databases. In this case , the database is 7500 transactions in a retail store collected over a week. 

It is very essential for effective Market Basket Analysis and it helps in understanding which items customers will buy together.
Such information can be used as the basis for decisions about marketing activities such as,promotional pricing , product placements, 
cross-selling and up-selling

## 3 parameters to be considered :

### Support : 
    - Support is an indication of how frequently the itemset appears in the dataset.
    - # times the product appears in the transaction / # total transactions
    
### Confidence : 
    - Confidence is an indication of how often the rule has been found to be true.
    - # transaction contains P1 and P2/ # transaction contains P1
    
### Lift(P1 -> P2) : Confifence(P1 -> P2)/Support(P1)
    - lift is the rise in probability of having {P2} on the cart with the knowledge of {P1} being present over the probability of having       {P2} on the cart without any knowledge about presence of {P1}.
    - If the rule had a lift of 1, it would imply that the probability of occurrence of the antecedent and that of the consequent are         independent of each other. When two events are independent of each other, no rule can be drawn involving those two events.
    - If the lift is > 1, that lets us know the degree to which those two occurrences are dependent on one another, and makes those           rules potentially useful for predicting the consequent in future data sets.
    - If the lift is < 1, that lets us know the items are substitute to each other. This means that presence of one item has negative         effect on presence of other item and vice versa.

## Steps followed in the algorithm :
- step1 : convert the dataset into list
- step2 : set a minimum support,confidence,lift
- step3 : take all the subsets in transactions having higher support than minimum support 
- step4 : take all teh rules of these subsets having higher confidence than minimum confidence
- step5 : sort the rules by decreasing lift 
