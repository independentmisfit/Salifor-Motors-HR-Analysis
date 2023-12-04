# Salifort-Motors-HR-Analysis
EDA and ML models to evaluate employee turnover rate at Salifort Motors
This project contains used to evaluates the reasons behind the massive employee turnover at a fiction company named Salifort motors. The project also covers the construction of predictive models for the Human Resourc department of the company on employee leaving or staying at the comapny. 
Yhe project was built with the Plan Analyze Construct and Execute (PACE) framework.
At the plan stage, focus was on understanding the business problem and the data. The business problem was further articulated as:
Understand the business scenario and problem
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data. They have the following question: what’s likely to make the employee leave the company?

Your goals in this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company.

If you can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.
The dataset that you'll be using in this lab contains 15,000 rows and 10 columns for the variables listed below and can be found on kaggle.
The folllowing deductions wer made in the plan stage:
The HR department and leadership team of Salifort Motors are the stakeholders for this project.
The aim of the project is to uncover the reasons behind employee turnover and build either a ststistical or machine learning model to predict if an employee would leave or stay in the company.
At this point of the project, most employees in the company have worked for less than 5 years.
I find myself consulting notebooks on performing certain basics EDA tasks such as Boolean Masking
Yes, the inclusion or exclusion of outliers in model development. Further revelation in the data would reveal the next action to take on this.
ANALYZE Stage:
The next step that followed was the ANALYZE stage, where Exploratory data analysis was carried out with various data visualizations and the following insights were uncovere:
The boxplot and histogram showing the average monthly hours and number works reveals that the more project worked on, the higher the monthly average hour worked. The visualization showed that for employees who have worked on 2 projects, majority of those who left worked less average monthly hours thab those who stayed. It is possible that such employees were fire for underperformance or were assigned fewer tasks based on previous notice of their departure. However for employees who have worked on 3-6 projects, most of these employees who left worked for more average monthly hours than those who stayed. And for employyes who worked on 7 projects, all left. This reveals that there are 2 classess of employees who left, those who worked less than their colleagues and those who worked significantly more. The employees who stayed and worked on 3-6 projects have a mean average monthly hour of 200, which means employees work about 46 hours weekly. It is possible that employees are overworked.
The scatter plot showing the relationship between average monthly hours and last evaluation reveals a high corellation betweens hours worked and evaluation score. It aslo revealed two classes of employees that left the company. Those who score about 50-60% in their last evaluation but worked for less than a monthly average of 167 hours, which is less than 38 hours per week. The second class of employees that left are those who scored high in their last evaluation (80-100%) and worked more than 250 hours per month on average, which is more than 57 hours per week. Hence, it can be said that employees who underwork and overwork left the company. A fair number of employees work slighly below or above 200 hours on average every month. This translates to 46 hours per week, well over the standard of 40. This indicates that the employees are overworked.
The scatterplot showing the relationship between average monthly hours and satisfaction level reveals that majority of employee who left the company had a satisfaction level of 50% or less. Of these employees, some worked less than 166.67 hours per month, which is less than 38 hours, and had a satisfaction rate of about 30 - 50%. The other group of employees who left worked for over 225 hoours per month on average, over 51 hours per week and had a satisfaction level of less than 20%. THese reveals that employees who left were deeply unsatisfied, and further corrobated the earlier analysis that revealed that employees who leave the company either underperform or over work. The scatter plot showed that majority of employees who stayed have a satisfaction level of 50% or more but are also over worked as revealed by the average monthly hours ov around 200, 46 hours per week.
Majority of employees who have left the company have spent less than 5 years at the company. As seen from the earlier visaulization, employees who have left the company have a satisfaction level lower than their colleagues. This is true for employess who have spent 4-2 years at the company. However employees who spent 5 and 6 years at the company and have left have a satisfaction level higher than those of their colleagues who have stayed. No employee who have stayed for over 6 years left the company. It is possible that employees who spent 5-6 yeras in the company and left, may have done so due to lack of promotion.
The scatter plot plotting promotion in the average monthly hours against promotion in the last 5 years, showed that majority of employees who have left the company are those who have overworked (more than 275 average monthly hours, 63 hours per week.) and have not been promoted in the last 5 years.
The departments mostly affected by employee turnover are Sales, Technical, Support, and IT.
Employees who have left the company have a low or medium salary.
CONSTRUCT stage:
In the construct stage three models were constructed, a tuned decision tree model, tuned random forest, and XGBoost model.
The data was split into a training, validation, and test set. The training set was used to get the right hyperparameters for each model, and the validation set was used to compare the results of each model to select the chapion model. The evaluation metric used to perform the comparision was recall, as the cost of a false negative would cost the company to continue to waste resources on employees who would leave the company.
The random forest model emerged as the champion model with a 91% recall value upon test on the testing dataset. However this gave concerns to data leaking, and the featuring engineering led to the the removal of the satisfaction_rate and amount_monthly_hours column and the creation of a overworked columns (employees who worked abover 167 hours on average). The column was encoded as 1 for yes, and 0 for no. 
The data was then divided into training, validation, and testing sets after the target and outcome variables had been splitted. The traing data was used to get the right hyper parameter for each model, and the validtion data was used to test the data to determine the champion model using the recall evaluation metric. 
The random forest model emerged as the champion model and upon testing on the test data, it revealed the following results:
a precision score of 0.905237, a recall score of 0.91206, accuracy score of 0.908636, fl score of 0.969571 and auc value of 0.946535.
The following conclusions and recommendations was made:
There should be cap on hours worked weekly, and if possible hours spent working overtime can be incentivized.
There should be review on promotion policies, and workers who work on more projects and hours, with great evaluation scores should be strongly considered.
There should be a review of policies for employees who have spent 3-5 years at the company as they seem to leave more often despite working longer hours.
There should be cap on projects undertaken by employees to prevent spending longer hours working. If employees take more projects than the cap, it should be voluntary and rewarded.
More feedback is required from employees who have spent 4-5 years in the compamy and have reported to be greatly satisfied, yet left the company.
