[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample.  
Use the NSFG respondent variable NUMKDHH to construct the actual distribution for the number of children under 18 in the household.   
>>Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.  
  
Plot the actual and biased distributions, and compute their means. (As a starting place, you can use chap03ex.ipynb)

```python
import nsfg    
```
Load Data
```python
    
    df2 = nsfg.ReadFemResp()
    ```
# Construct Distribution
```python
pmf=thinkstats2.Pmf(resp.numkdhh, label='Children<18')
```
compute biased distribution
```python
biased_pmf=BiasPmf(pmf, label='Biased')
```

Plot actual and biased distribution
```python
pmf.label='Actual'
thinkplot.preplot(2)
thinkplot.Pmfs([pmf,biased_pmf])
thinkplot.config(xlabel='Children under 18', ylabel='PMF')
```

Compute actual & biased mean
```python
print('Actual Mean:',pmf.Mean())
print('Biased Mean', biased_pmf.Mean())
```
Actual Mean: 1.02420515504
Biased Mean 2.40367910066


### Response
The actual mean of 1.02 is below the observed mean of 2.40 because, for a survey taken by asking the children, children in big families would overrrepresent their families and
families with no children would not be represented at all.  
    

   
