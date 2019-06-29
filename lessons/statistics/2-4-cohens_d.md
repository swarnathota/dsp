[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

from thinkstats2 import CohenEffectSize 
# importing CohenEffectSize from the authours code(thinkstats2.py)

live = df[df.outcome == 1] #Live babie are into account. 

first = live[live.birthord == 1].totalwgt_lb    # subsetting total weight of the first born babies  

others = live[live.birthord != 1].totalwgt_lb    # subsetting total weight of the otherthan first born



CohenEffectSize(first, others)       #Cohen's D which is equal to -0.886

# Cohen's D, effect size, answers the question how much effect either first born or second born have an effect on baby weight. Inorder to find cohens'D, calulate mean of first born and other babies and find pooled standardndeviation. Difference of means is divided by pooled standared deviation. If Cohen'D is negative that suggests that effect size is favouring towards right hand side group. We usually  
# In the above example, Cohen'D was found out to be -0.0886 suggesting that effect is more towards other babies except first. 

first_prglength = live[live.birthord == 1].prglngth      # subsetting pregnant length of the first born babies 

other_prglength = live[live.birthord != 1].prglngth      # subsetting pregnant length of the first born babies

first_prglength.std(), other_prglength.std()        # standard deviation of fisrt pregnancy length and second pregnancy length

CohenEffectSize(first_prglength, other_prglength)  

# In the above example, Cohen's D was found to be 0.0288 suggesting that the first born has more effect than others.
