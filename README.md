# Salifort-Motors-HR-Analysis: README
Overview
The Salifort-Motors-HR-Analysis project aims to predict employee turnover at Salifort Motors by employing exploratory data analysis (EDA) and machine learning models. The project's primary goal is to understand and address the significant employee turnover issue within the fictional company, Salifort Motors. The predictive models built in this project intend to assist the Human Resources department in identifying factors leading to employee departure, enabling proactive measures to improve employee retention.

Business Understanding
Salifort Motors' Human Resources department seeks data-driven insights to enhance employee satisfaction levels within the company. The collected dataset, available on Kaggle, comprises 15,000 rows and 10 columns. The project's focus involves unraveling the causes behind employee turnover and constructing statistical or machine learning models capable of predicting employee retention or departure.

Data Understanding
During the data understanding phase, various visualizations provided essential insights into the relationship between different variables and employee turnover at Salifort Motors:

Workload and Projects: The boxplot and histogram analysis of average monthly hours versus the number of projects revealed distinct patterns. Employees working on different project volumes displayed varying tendencies regarding average monthly hours worked. Those leaving the company fell into two classes: those working significantly less than their colleagues and those working substantially more, indicating potential underperformance or overloading issues.

Work Hours and Evaluation Scores: The scatter plot analysis of average monthly hours against the last evaluation score highlighted a correlation between working hours and evaluation scores. Two classes of departing employees emerged: those with moderate evaluation scores but worked below average hours and those with high evaluation scores but overworked, suggesting a trend where both underworking and overworking employees left the company.

Work Hours and Satisfaction Level: Another scatterplot depicting average monthly hours against satisfaction level revealed that departing employees predominantly had satisfaction levels of 50% or less. Employees leaving the company were deeply unsatisfied, with a majority either underperforming or being overworked, corroborating earlier analyses.

Employee Tenure and Satisfaction: Employees leaving the company mostly had less than 5 years of tenure. Interestingly, those with 5-6 years of tenure, leaving the company, exhibited higher satisfaction levels than their counterparts who stayed, potentially indicating a lack of promotion as a reason for their departure.

Promotion and Work Hours: The scatter plot analyzing promotion, average monthly hours, and promotions in the last 5 years highlighted that most departing employees were those who overworked and had not been promoted in the last 5 years.

Affected Departments: Employee turnover predominantly affected departments such as Sales, Technical, Support, and IT.

Salary Impact: Departing employees mostly had low or medium salary ranges.

These comprehensive visualizations and analyses shed light on the interconnectedness of workload, evaluation scores, satisfaction levels, tenure, promotions, and departmental impacts on employee turnover at Salifort Motors. Understanding these factors plays a crucial role in constructing predictive models and devising strategies to mitigate employee turnover within the company.
Modeling and Evaluation
The project utilized the Plan Analyze Construct and Execute (PACE) framework. In the Analyze stage, detailed EDA was conducted using various visualizations. Insights obtained from this stage highlighted correlations between factors such as average monthly hours worked, satisfaction levels, evaluation scores, and employee departures. It was observed that employees leaving the company fell into two categories: those working significantly less than their colleagues and those working extensively more. Additionally, a correlation between satisfaction levels, working hours, and employee turnover was established.

In the Construct stage, three models—tuned decision tree, tuned random forest, and XGBoost—were developed. The dataset was split into training, validation, and test sets for model training and evaluation. The primary evaluation metric used was recall, given the cost implications of false negatives on employee retention. The random forest model emerged as the champion model, initially showing a 91% recall value. However, concerns regarding data leakage prompted feature engineering, removing columns like satisfaction rate and average monthly hours, creating a new 'overworked' column. The refined random forest model achieved significant performance with a precision score of 0.905237, recall score of 0.91206, accuracy score of 0.908636, F1 score of 0.969571, and an AUC value of 0.946535 upon testing.
Conclusion with Recommendations
The Salifort-Motors-HR-Analysis project has provided valuable insights into the factors contributing to employee turnover at Salifort Motors. The constructed random forest model, with its high performance in predicting employee departures, offers significant guidance for proactive Human Resources strategies to improve employee retention within the company.

Recommendations:

Address Workload Balance: The analysis revealed a dichotomy in employee departures: those who work significantly less than their colleagues and those who work extensively more. Addressing workload disparities could involve workload redistribution, clear task assignment, and potentially reconsidering the hours required from employees.

Focus on Employee Satisfaction: The correlation between dissatisfaction and departures underscores the importance of enhancing employee satisfaction levels. Conducting surveys, implementing feedback mechanisms, and actively addressing concerns raised by employees could boost overall satisfaction and consequently reduce turnover.

Promotion and Career Growth: Employees staying for over five years, particularly those leaving between the 5-6 year mark, may indicate a lack of career growth or promotion opportunities. Implementing clear pathways for career advancement, recognizing long-term employees' contributions, and facilitating growth opportunities might retain experienced talent.

Departmental Strategies: Given the significant turnover in departments like Sales, Technical, Support, and IT, implementing specific retention strategies tailored to these departments could prove beneficial. Understanding departmental dynamics and addressing their unique concerns may improve retention rates.

Salary and Rewards: Reviewing salary structures and employee rewards could play a pivotal role in enhancing job satisfaction and reducing turnover. Offering competitive compensation aligned with industry standards and recognizing outstanding performances could boost employee morale.

Continual Monitoring and Adjustment: Implementing a system for continuous monitoring of employee satisfaction, workload distribution, and career growth opportunities is crucial. Regularly reassessing and adjusting HR strategies based on ongoing data analysis ensures a proactive approach to employee retention.

By implementing these recommendations based on the insights derived from the analysis and the predictive model, Salifort Motors can take proactive steps toward reducing employee turnover, fostering a healthier work environment, and ultimately improving the company's overall performance and stability.




