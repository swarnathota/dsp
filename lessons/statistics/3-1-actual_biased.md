[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    import probability
    import thinkstats2
    
    resp = nsfg.ReadFemResp() # Reads the NSFG respondent data and returns dataframe
    d = resp['numkdhh']
    pmf = thinkstats2.Pmf(d, label = 'numkdhh(actual)') # Calculates PMF for number of children
    pmf.Mean() # Mean of pmf
    thinkplot.pmf(pmf) # Plots pmf vs Number of children
    thinkplot.Config(xlabel = 'Number of children', ylabel = 'Pmf')
    
    
    
    
    
    from probability import BiasPmf  
  
 
    biaspmf = BiasPmf(pmf, label = 'BiasedPmf(observed)') # BiasPmf calculates distribution as observed by students 
    biaspmf.Mean()
    thinkplot.Pmf(biaspmf)
    thinkplot.Config(xlabel = 'Number of children', ylabel = 'BiasedPmf')
    
    
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biaspmf])
    thinkplot.Config(xlabel = 'Number of children', ylabel = 'PMF')
    
    
    
    
    
    
    
