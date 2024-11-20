# ClearCutCostumerClustering
CCCC: Clear Cut Costumer Clustering (with some Classification)

## Folder Structure 
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



## Aligment rules

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
 
