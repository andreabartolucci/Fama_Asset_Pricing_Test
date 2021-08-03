# Fama_Asset_Pricing_Test
The script performs the classic Fama asset pricing test of a set of factors against multiple set of portfolios. The script is flexible, the user can pass a set of factors in a file a multiple set of test asset portfolios in another file. All the test summary metrics in Fama and French (2015, 2016) are calcluated.

The script pretty much replicates the table t of Fama and French (2015). The screenshot is inside the notebook. The first difference is that only one set of factors is tested, therefore the table would only have one group of columns, for instance 2x3 if the user passes this set of factors. The second difference is that only a model with all the factors passed is estimated (no permutations), therefore the table below would only include une row for each panel with the list of all the factors, for instance only HML RMW CMA for each panel in the table below.

The script contains all the basic elements, the user is free to wrap the script into an outer loop on a list of factors sets, and an inner loop to test permutation with subsets of factors for each set of factor.

The user can pass a set of factors and a collection of multiple sets of test assets, similar to the table below (there 6 panels). The script test the set of factor against all the test asset sets and calculate different metrics (the one in the table below plus those used in Fama and French (2016)).

The output contains on each row the result of one regression (one portfolios regressed on the set of factors). Part of the columns dynamically will contain the name of the factors passed by the user (the factors coefficients, the factors pv, and the factors t-stat). For instance the columns would be:
- reg_n
- test_ptf_set_n
- obs
- nfactors
- formed_on
- ptf_n
- test_ptf
- factors_list
- Mkt-RF
- SMB
- HML
- CMA
- RMW
- XMY
- Mkt-RF_pv
- SMB_pv
- HML_pv
- CMA_pv
- RMW_pv
- XMY_pv
- Mkt-RF_tstat
- SMB_tstat
- HML_tstat
- CMA_tstat
- RMW_tstat
- XMY_tstat
- alpha
- alpha_pv
- alpha_tstat
- R2
- avg_R2
- Adj_R2
- avg_Adj_R2
- GRS
- GRS_pVal
- A|a|
- A|a|/A|r|
- A(a^2)/A(r^2)
- As^2(a)/A(a^2)]

![image.png](attachment:image.png)
