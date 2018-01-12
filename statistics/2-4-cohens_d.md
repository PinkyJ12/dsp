[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>  Compute the Cohen effect size for the difference in pregnancy length for first babies and others.  
>> ```python
>> lenEffect = CohenEffectSize(firsts.prglngth, others.prglngth)
>> print(lenEffect)
>> ```
>> 0.0288790446544


>>
>> Compute the Cohen effect size for the difference in birth weight for first babies and others.  
>> ```python
>> wgtEffect = CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
>> print(wgtEffect)
>> ```
>> -0.0886729270726
>>
>> Compare the effect sizes.  
>> ```python
>> effectDiff = np.abs(wgtEffect) - np.abs(lenEffect)
>> print(effectDiff)
>> ```
>> 0.0597938824182
>>
>> Birth order has a greater effect on birth weight than on pregnancy length.
>>
