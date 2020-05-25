#  An exploratory data analysis on Behavioral Risk Factor Surveillance System (BRFSS)

Data information is from [BRFSS Overview](https://www.cdc.gov/brfss/annual_data/2013/pdf/Overview_2013.pdf)

The Behavioral Risk Factor Surveillance System (BRFSS) is a collaborative project between all of the states in the United States (US) and participating US territories and the Centers for Disease Control and Prevention (CDC). The BRFSS is administered and supported by CDC’s Population Health Surveillance Branch, under the Division of Population Health at the National Center for Chronic Disease Prevention and Health Promotion. BRFSS is an ongoing surveillance system designed to measure behavioral risk factors for the non-institutionalized adult population (18 years of age and older) residing in the US. The BRFSS was initiated in 1984, with 15 states collecting surveillance data on risk behaviors through monthly telephone interviews. Over time, the number of states participating in the survey increased; by 2001, 50 states, the District of Columbia, Puerto Rico, Guam, and the US Virgin Islands were participating in the BRFSS. Today, all 50 states, the District of Columbia, Puerto Rico, and Guam collect data annually and American Samoa, Federated States of Micronesia, and Palau collect survey data over a limited point- in-time (usually one to three months). In this document, the term “state” is used to refer to all areas participating in BRFSS, including the District of Columbia, Guam, and the Commonwealth of Puerto Rico.

The BRFSS objective is to collect uniform, state-specific data on preventive health practices and risk behaviors that are linked to chronic diseases, injuries, and preventable infectious diseases that affect the adult population. Factors assessed by the BRFSS in 2013 include tobacco use, HIV/AIDS knowledge and prevention, exercise, immunization, health status, healthy days — health-related quality of life, health care access, inadequate sleep, hypertension awareness, cholesterol awareness, chronic health conditions, alcohol consumption, fruits and vegetables consumption, arthritis burden, and seatbelt use. Since 2011, BRFSS conducts both landline telephone- and cellular telephone-based surveys. In conducting the BRFSS landline telephone survey, interviewers collect data from a randomly selected adult in a household. In conducting the cellular telephone version of the BRFSS questionnaire, interviewers collect data from an adult who participates by using a cellular telephone and resides in a private residence or college housing.

Health characteristics estimated from the BRFSS pertain to the non-institutionalized adult population, aged 18 years or older, who reside in the US. In 2013, additional question sets were included as optional modules to provide a measure for several childhood health and wellness indicators, including asthma prevalence for people aged 17 years or younger.



### Review some useful concepts 
Form [Introduction to Probability and Data course offered by Duke university](https://www.coursera.org/learn/probability-intro)

Observational studies can provide evidence of a naturally occurring association between variables, but they cannot by themselves show a causal connection. Researchers perform an observational study when they collect data in a way that does not directly interfere with how the data arise. For instance, researchers may collect information via
surveys, review medical or company records, and etc.

When researchers want to investigate the possibility of a causal connection, they conduct an experiment. To check if there really is a causal connection between the explanatory variable and the response, researchers will collect a sample of individuals and split them into groups. The individuals in each group are assigned a treatment. When individuals are randomly assigned to a group, the experiment is called a randomized experiment.

There is a good table categorizing these concepts from the course video in the week 1. It emphasizes that most of the observational studies have random sampling but not random assignments and therefore are not casual , but generalizable:

<center>

![Table 1. random assignments and sampling table from the course video](img/ran_sam.jpg) 

</center>




Let's now investigate BRFSS dataset:

Based on what we have reviewed, we can say that BFRSS survey is an **observational study**. The reason is that in conducting the BRFSS landline telephone survey, interviewers collect data from a randomly selected adult in a household. We only have chosen samples randomly through selected adults, therefore resulted sample may represent the population. So,this study is generalizable to the population at large. However,Since 2011 BRFSS conducts both land-line telephone- and cellular telephone-based surveys. For the cellular telephone-based surveys, interviewers collect data from an adult who participates by using a cellular telephone and resides in a private residence or college housing. This part of the study is not randomly selected. Therefore, it may raise convenience bias. So, for this part, we would not generalize the sample to the whole population.  

On the other hand, since the study does not use of any random assignment, it can't be used for causality study.Random assignment only occurs in experimental settings. Through random assignment we ensure that different characteristics are represented equally in treatment and control groups. Also, random assignment allows us to make causal conclusions based on the study. 


* * *

## Part 2: Research questions

In this part, we want to contemplate some research questions. 
The BRFSS objective is to collect uniform, state-specific data on preventive health practices and risk behaviors that are linked to **chronic diseases**, **injuries**, and **preventable infectious diseases** that affect the adult population.Thus, it would be interesting to look at some factors like tobacco use, HIV/AIDS knowledge and prevention, exercise, immunization, health status, healthy days — health-related quality of life, health care access, inadequate sleep, hypertension awareness, cholesterol awareness, chronic health conditions, alcohol consumption, fruits and vegetables consumption, arthritis burden, and seatbelt use.


**Here I will only investigate 3 research questions:**


**Research question 1:**

As a first question, we might be interested in exploring the factors may have a relationship with the chronic diseases like heart attach. Some of the factors seem more likely to have relationship with are:

- Hypertension awareness,
- Cholesterol awareness, 
- Alcohol consumption
- Exercise 
- Tobacco use 

For the first question I'd like to focus on some of the above factors. From the codebook I will choose the below columns and variables to specifically investigate heart attack case:


- **cvdinfr4**: Ever Diagnosed With Heart Attack

- _**rfchol**: High Cholesterol Calculated Variable

- _**rfsmok3**: Current Smoking Calculated Variable

- _**rfhype5**: High Blood Pressure Calculated Variable



**Research question 2:**

As a second question, I will look at the relationship between having diabetes 
and factors like age , and sugar consumption. We may have an idea that sugar consumption is one of the factors of having diabetes. Also, we might be interested on relationship between age and diabetes. For both of these variables we need to look at the codebook and explore them more.
Thus, form the codebook I will choose the below columns and variables:


- **diabete3:** (Ever Told) You Have Diabetes

- **diabage2:** Age When Told Diabetic
 
- **ssbfrut2:** How Often Did You Drink Sugar-Sweetened Drinks?



**Research question 3:**

For the third question, we might be interested in exploring the relationship between exercise and metal health status.

Finally, for this question, form the codebook I will choose the below columns and variables:


- **exerany2:** Exercise In Past 30 Days

- **misdeprd:** How Often Feel Depressed Past 30 Days

- **mishopls:** How Often Feel Hopeless Past 30 Days

* * *

**Now, If you are intersted in this project, please look at the R markdown or HTML file for EDA analysis of this project.** 
