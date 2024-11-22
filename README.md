# ClearCutCostumerClustering
CCCC: Clear Cut Costumer Clustering (with some Classification)

## Summary
The project is to provid a cluster label.

Data Analyst Business:
• Perform robust exploratory analysis, rich with business insights & data driven proposals to add value to the company and have strong communication skills to influence the decision making

Data Advanced Analytics
• Perform robust exploratory analysis, using advanced analytics tools and statistical methods to generate data products to optimize business results (predictive & clusterization models, for example)

You will be able to see some of the steps we created in the issues section of the repo. These steps are still underdevelopment. When we start working on the dataset we will see what's still needed.

Based on our intial discussions and data exploration we were able to think about two different approchaes to the issue.

### - Approach A:

Approach A is **a two chained models(a classifer then a clusterer)** in order to deal with new customer data. In this approach we started from the Goal trying to reverse engineer the task. We imagned how would the new data come in?

New data would most probably come in without the features AcceptedCmp1 - AcceptedCmp5 which refer to which previous marketing Campaigns has each customer accepted.
In this case **we will be missing imporant data that refers to an important customer habit** 

So in order to bypass this issue:

- we thought about a **classifer** that first labels the customers to Interested in campaigns (Label 1) and not that interested in campaigns (Label 0).

    Label 1: Customers who accepted more than 3 out of 5 campaigns
    Label 0: Customers who accepted between 0 and 2 campaigns

- Now we have the Label feature we can drop the AccptedCmp1 - AcceptedCmp5 as new customers will not have these data.

- When we add the Label feature we will be able to treat it as a normal classifer and split the dataset, train, val, test.

- After we classify and make sure the Classifer is working fine we move to the second model which is the clusterer.

- In this step we take the Labeled 0 customers and cluster them into clusters which we will develop a marketing stratgey for each.

**Expected output**

When we recive new data for a customer, we can pass it through the classifer first to see if they are 1 or 0.

If 1 , Send the campaign to them based on their highest two spending catergories.
if 0 , Select which cluster to assign to then apply the needed stratgy based on the cluster.

(Marketing stratiges to be developed further when we reach good working models)

### Approach B:

We will work in a straight line towards the clustering.

- EDA
- Choosing a model
- Evaluate the model
- Tune the parameters
- Evaluate the model again

Check the clusters based on the most imporant features and develop a marketing stratiges based on that.



### Folder Structure 
```sh
├── code             # python scripts or jupyter notebooks
├── data
│   ├── 01_input     # input data
│   ├── 02_inter     # intermediate data for further analysis
│   └── 03_output    # output data
├── documentation    # documentation                                               (will it remain empty? surely not, right?)
├── output
│   ├── figures      # nice figures
│   └── tables       # nice tables
├── resources        # resources for project
├── versions         # why do we have this folder again?
└── zz_trash         # unused files that could actually be deleted.
```



### Aligment rules

- The variable for the dataset is `df`.
- naming features:
  -  `snake_case`
      -  Kidhome -> kid_home
  -  bad: sum_all_mnt
  -  good: mnt_all_sum
  -  better: amount_spent_total
     -  (`_total` at the end, so that it groups nicely with `amount_spent_average` and `amount_spent_variance`, etc) 
- for each cell/process, write a comment on what you are doing.
  - remove the comment if they are no longer relevant!
- name your functions meaningfully. 
 
