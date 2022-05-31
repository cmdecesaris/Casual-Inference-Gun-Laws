

# Casual-Inference-Gun-Laws
For full report see: https://rpubs.com/cmdecesaris/742740

# Abstract

Using panel data regarding violent crime, demographics, and gun control laws in the United States between 1977-1999, the effect of shall-carry gun laws on rates of violent crime among 50 states and the District of Colombia were investigated using a Propensity Weighted Linear Mixed Effects model. The model attempted to answer if a causal relationship could be determined between shall-carry laws and violent crime using robbery rates, murder rates, population density, and the percentage of young males between 10-29 years old as confounders. State and year were defined as random effects by the model. To reduce the selection bias introduced by confounders, propensity scores were calculated using a logistic regression model and weights were derived using the Inverse Probability of Treatment Weights method (IPTW). The final weighted model indicated a negative correlation between law=‘yes’ (p < 0.1) and violent crime rates. The significance of law was reduced after adding the weights suggesting some selection bias was removed from weighting. Murder (p < 0.05), robbery (p < 0.001), and young male population percent (p < 0.001) were found positively correlated with violent crime. Because selection bias was reduced but not eliminated, a causal relationship could not be determined.

# Introduciton and Background

The controversy surrounding guns has become a hotbed for political discourse in recent years. Some have linked gun ownership to increases in homicides, suicides, and organized criminal activity (Miller et. al, 2002). A 2004 publication found that owning a gun makes a person three to five times more likely to die by violence (Zimring). Others have suggested that gun ownership does not lead to a net increase in crime but rather increased crime leads to more gun ownership. In the case of this argument, authors argued that gun control laws would be ineffective in reducing violent crime (Kleck et. al, 2002). 

In this project, we investigate the relationship between population demographics, various crime rates, and shall carry gun laws across different regions of the United States between 1977-1999. Shall carry gun laws are laws which allow only licensed, trained, and background checked citizens to carry concealed guns in specific states. 


We seek to answer the following questions:

1. What is the effect of shall carry laws on violent crime in the United States?

2. Is this relationship casual?

It is important to note that a key point regarding the theory of causal interference is the factor variable in question should be changeable. In the case of this project, the shall-carry law in effect is a factor which can be implemented or rescinded by law makers making it ideal for this analysis. 

# Conclusion

This project used the panel Guns dataset from the AER package and analyzed the relationship between young male population percentage, population density, murder rates, shall-carry laws, and robbery rates and violent crime. The data was collected at the state level over the period between 1977-1999.

It was assumed that young male population percentage, population density, murder rates, and robbery rates had confounding effects on both violent crime and the implementation of shall-carry laws.

The main question of interest was whether the relationship between shall-carry laws and violent crime was casual. A propensity score weighted linear mixed effects model was fit to answer this question. State and year were regarded as random effects. Violent crime rate was the response and young male population percentage, population density, murder rates, shall-carry laws, and robbery rates were predictors.

To reduce selection bias introduced by our confounders on shall-carry laws, a logistic regression model using law as response and confounders as predictors was fit. These fitted values (propensity scores) were then converted into weights and applied to the final linear mixed model.

Balancing analysis suggests the weights only sucessfully achieved balanced between law and young male percentage. While imbalance may have been reduced among the treatment (law) and other confounders, it was far from eliminated.

The final weighted model indicated a negative correlation between law=‘yes’ and violent crime rates. The significance of law was reduced after adding the weights suggesting some selection bias was removed from weighting. Murder, robbery, and young male population percent were positively correlated with violent crime.

From the sensitivity analysis, model assumptions were roughly followed and the model was deemed adequate. It is possible that the assumption of no unobserved confounders was violated as not all data variables were included in the model.

Overall, we can NOT infer a causal relationship between shall-carry laws and violent crime rates because selection bias remains in the model.

The shall-carry law was also not highly, significantly correlated with violent crime rates which may grant merit to the cited studies which claimed gun control laws were ineffective in reducing violence (Kleck et. al, 2002).

# Running the Project

The project can be run by cloning the repository into one's R studio. There is no code or data not included within the repository. The loaded packages (best viewed in the main report) must be installed on one's local R studio. An html and pdf version of the report will be avaible for download. The interactive graphs and tables will be static in the pdf version of the report. 
