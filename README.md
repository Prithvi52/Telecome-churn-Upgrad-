# Telecom Churn Case Study

#Business Problem Overview

In the telecom industry, customers are able to choose from multiple service providers and actively
switch from one operator to another. In this highly competitive market, the telecommunications
industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10
times more to acquire a new customer than to retain an existing one, customer retention has
now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business
goal.

To reduce customer churn, telecom companies need to predict which customers are at high
risk of churn.

In this project, you will analyse customer-level data of a leading telecom firm, build predictive
models to identify customers at high risk of churn and identify the main indicators of churn.

# Understanding and Defining Churn

There are two main models of payment in the telecom industry - postpaid (customers pay a
monthly/annual bill after using the services) and prepaid (customers pay/recharge with a
certain amount in advance and then use the services).

In the postpaid model, when customers want to switch to another operator, they usually inform
the existing operator to terminate the services, and you directly know that this is an instance of
churn.

However, in the prepaid model, customers who want to switch to another network can simply
stop using the services without any notice, and it is hard to know whether someone has
actually churned or is simply not using the services temporarily (e.g. someone may be on a trip
abroad for a month or two and then intend to resume using the services again).

Thus, churn prediction is usually more critical (and non-trivial) for prepaid customers, and the
term ‘churn’ should be defined carefully. Also, prepaid is the most common model in India and
Southeast Asia, while postpaid is more common in Europe in North America.

This project is based on the Indian and Southeast Asian market.


# Steps Followed
1.Reading, understanding and
2.visualising the data

3.Preparing the data for
modelling

4.Building the model

5.Evaluate the model


# Reading, Understanding and Visualising
the Data

1. Importing DataSet

2. Reading And Understanding the Dataset

Data Shape - (99999,226)

Data info

Data describe

3. Handling Missing Data

4. Eliminating the data columns as the data columns are not required in our examination

Dropping columns as the column has only 1 unique value.

5. Filtering High Rise Customers

Creating column avg_rech_amt_6_7 by summing up total recharge amount of month 6 and 7. Then taking the
average of the sum.

Obtaining the 70th percentile of the avg_rech_amt_6_7

Customers who have recharged more than or equal to 10, Filter taht customers.

Data Shape = (30011, 178)


6. Handling the Missing Values in Rows

Here we are checking various missing values in the columns and removing the columns
accordingly to optimise the data for evaluation.

7. Tag Churners

Presently label the beat clients (churn=1, else 0) in light of the fourth month as follows: The
people who have not settled on any decisions (either approaching or friendly) AND have not
utilized portable web even once in the stir stage.

Eliminating all the attributes corresponding to the phase in churn

Checking Churn Percentage = 3.39

8. Outliers Treatment

In the separated dataset aside from mobile_number and stir segments every one of the
sections are numeric sorts. Subsequently, changing over mobile_number and stir datatype to
protest.

Removing the outliers which are below 10th and are above 90th percentile

Data Shape= (27705, 136)

9. Taking in New features

Deriving new column

Decrease_mou_action

Decrease_rech_num_action

Decrease_rech_amt_action

decrease_arpu_action

decrease_vbc_action


# Exploratory Data Analysis (EDA)

# Univariate Analysis

On the basis on the churn rate whether the
customer decreased his MOU in action month

We can obviously see that the agitate rate is
something else for the clients, whose minutes
of usage(mou) diminished in the activity stage
than the great stage.

Agitate rate on the premise whether the client
diminished his/her number of re-energize in real
life month

True to form, the agitate rate is something else
for the clients, whose number of re-energize in
the activity stage is lesser than the number in
great stage


Agitate rate on the premise whether the
client diminished his/her measure of
re-energize in real life month

Here additionally we can plainly see that a
similar way of behaving. The stir rate is
something else for the clients, whose measure
of re-energize in the activity stage is lesser than
the sum in great stage


Churn rate on the premise whether the
client diminished his/her volume based
cost in real life month

The churn rate is something else for the clients,
whose volume based cost in real life month is
expanded. That implies the clients don't do the
month to month re-energize more when they are
in the activity stage. Here we can see the normal
outcome.


Examination of the typical income per
client (churn and not churn) in the activity
stage

Normal income per client (ARPU) for the churned
clients is generally densed on the 0 to 900. The
higher ARPU clients are more averse to be
churned.

ARPU for the not churned clients is generally
densed on the 0 to 1000.

