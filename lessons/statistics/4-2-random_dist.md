[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    import thinkststs2
    import thinkplot
    import cumulative
    import random
    num = np.random.random(1000) # generates random variables 
    pmf = thinkstats2.Pmf(num)  #using the function Pmf (probability mass function) thinkstats2
    cdf = thinkstats2.Cdf(num) #using cumulative distribution function from authors code.
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel = 'variables', ylabel = 'CDF')
    thinkplot.Pmf(pmf, linewidth = 0.05)
    thinkplot.config(xlabel='variables', ylabel='PMF')
