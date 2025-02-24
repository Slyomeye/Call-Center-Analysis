# Call-Center-Analysis
I developed a comprehensive project in Power BI, creating multiple dashboards to analyze the data. This process involved several stages, including data preprocessing, data cleaning and data visualization.
##Objective
This is to analyze a call center dataset using Power BI to uncover insights and trends that can drive operational improvements and enhance customer satisfaction.
## Project Goals
•	Operational Performance: To identify performance trends of agents over time.
•	Topic Trends: To analyze the distribution of call topics.
•	Agent Performance: To measure operational metrics such as resolution rates, speed of answer and talk duration,
•	Customer Insight: Correlate satisfaction ratings with various factors to determine key drivers of customer satisfaction.
## DATA PREPARATION
Dataset[
Line Chart: To Show trends over time
Stacked Bar/Column Chart: To Break down total Values into subcategories
Heatmap: The use of colors to represent values in the matrix table format
Area Chart: To show cumulative data trends over time
Pie Chart: To display proportions of a categories using slices of a circle
Data Cleaning in Power Query
•	Removed duplicates based on call ID
•	Ensured all dates and times are well formatted
•	Handled missing/null values by replacing them in the critical fields.
 Data Transformation
•	Used DAX to create new measures such as Resolution rate, answer rate, total speed of answer, total call duration per agent, average speed of answer, average satisfaction rating, answered calls, resolved calls, total calls, day, Month.
•	Resolution Rate = DIVIDE(COUNTROWS(FILTER(Sheet1, Sheet1[Resolved] = "Yes")), COUNTROWS(Sheet1)) * 100
•	Answer Rate = DIVIDE(COUNTROWS(FILTER(Sheet1, Sheet1[Answered (Y/N)] = "Yes")), COUNTROWS(Sheet1)) * 100
•	Answered Calls = COUNTROWS(FILTER(Sheet1, Sheet1[Answered (Y/N)] = "Yes" ))
•	Average Satisfaction Rating = AVERAGE(Sheet1[Satisfaction rating])
•	Resolved Calls = COUNTROWS(FILTER(Sheet1,Sheet1[Resolved] = "Yes"))
•	Total Calls = COUNT(Sheet1[Call Id])
•	Unresolved calls = COUNTROWS(FILTER(Sheet1, Sheet1[Resolved] = "No"))
•	Month = FORMAT(Sheet1[Date], "mmmm")
•	Total Call Duration = SUM(Sheet1[AvgTalkDuration])

KPI’s (Key Performance Indicators)
•	Total Calls
•	Answered Calls
•	Resolved Calls
•	Resolution Rate
•	Average Speed of Answer

Dashboard[
Visual filters(slicers) were added for three fields named “Agent”, “Topic” and “Day”.
Five(5) Text Box visuals were  added to the canvas;  representing “Total Calls”, ”Answered Calls”, “Resolved Calls”, “Resolution Rate” and “Average Speed of Answer”.
Created Paginated reports from the data so as to uncover insights.
## INSIGHTS
After comparing resolution rates, satisfaction rates by agent, I was able to identify top performing agents and areas for improvement. By analyzing the resolved versus unresolved calls I was able to evaluate the effectiveness of agents and also a slower speed of answer may correlate with lower satisfaction or call abandonment. A high percentage of unanswered calls may indicate issues in call handling or staffing levels. By visualizing call trends over time, I was able to identify peak periods and certain topics may generate more calls and lead to lower satisfaction rating.

#RECOMMENDATIONS
•	Provision of trainings or support agents to agents with lower satisfaction rating and resolution ratings to enable customer satisfaction. These trainings can be in from of better call handling techniques, how to improve their empathy and communication skills.
•	Monitor key performance indicators (KPI’s) like speed of answer, resolution rate, satisfaction and answered calls and establish performance thresholds so that KPI’s are met but if they’re not met, then trigger investigations to address the root cause.
•	Customer feedback should be integrated to get more details after each call so as to help identify issues affecting satisfaction and enable quicker resolution.
•	In the issue of certain topics being more common and generating high call volumes, a self-service improvement expansion in form of automated chatbots, should be considered to resolve the issues without needing agent intervention.
•	Improvement of call routing by Implementation of automated call routing systems that direct calls based on topics or issues to the most appropriate agent thereby increasing resolution efficiency and reducing response time.
•	Staff optimization by increasing number of agents during peak volume times to manage call load and reducing staff during low volume times with the use of time monitors to adjust staff dynamically.
