# Practicum_project_9
 My ninth project from Practicum course. "Integrated Project #2. User behavior and A/A/B test for the company's app"
 
 What was used in the project: Python, Jupyter notebook. Libraries: pandas, numpy, plotly, matplotlib, seaborn, scipy.

# Project Description

I work at a startup that sells food products. I need to investigate user behavior for the company's app.<br/>
The designers would like to change the fonts for the entire app, but the managers are afraid the users might find the new design intimidating. They decide to make a decision based on the results of an A/A/B test.<br/> 
The users are split into three groups: two control groups get the old fonts and one test group gets the new ones. I need to find out which set of fonts produces better results.

# Steps
1) Prepare the data for analysis.
2) Study and check the data.
    - What period of time does the data cover? Find the maximum and the minimum date. Plot a histogram by date and time. Older events could end up in some users' logs for technical reasons, and this could skew the overall picture. Find the moment at which the data starts to be complete and ignore the earlier section.
    - Did I lose many events and users when excluding the older data?
3) Study the event funnel.
    - See what events are in the logs and their frequency of occurrence. Sort them by frequency.
    - Find the number of users who performed each of these actions. Sort the events by the number of users. Calculate the proportion of users who performed the action at least once.
    - In what order the actions took place.
    - Use the event funnel to find the share of users that proceed from each stage to the next.
    - What share of users make the entire journey from their first event to payment?
4) Study the results of the experiment.
    - How many users are there in each group?
    - We have two control groups in the A/A test, where we check our mechanisms and calculations. See if there is a statistically significant difference between samples 246 and 247.
    - Select the most popular event. In each of the control groups, find the number of users who performed this action. Find their share. Check whether the difference between the groups is statistically significant. Repeat the procedure for all other events.
    - Do the same thing for the group with altered fonts. Compare the results with those of each of the control groups for each event in isolation. Compare the results with the combined results for the control groups.
    - What significance level should I set to test the statistical hypotheses mentioned above?
  
# Description of the data

The data is stored in file logs_exp_us.csv

Columns:

'EventName'<br/>
'DeviceIDHash' — unique user identifier<br/>
'EventTimestamp'<br/>
'ExpId' — experiment number: 246 and 247 are the control groups, 248 is the test group
