# Project 1: Social Media

In this project, our group applied Pandas algorithms using Python to study the impact of social media on mood.

SETUP

We began by collectively deciding upon a topic that we wanted to explore. We eventually stumbled upon a survey from 2017 that sampled a population that would check their social media devices. After every recorded social media session, each participant would record their stress levels on a scale of 1 to 10 from different angles. The emotions tracked were:
  * Ability to concentrate
  * Depression
  * Fatigue
  * Hopelessness
  * Feelings of inferiority
  * Loneliness
  * Loss of interest
  * Stress

In order to make critical judgments about this data, we first cleaned the data using Pandas dataframes in Python, ensuring that all results were consistent and that we weren't skewing the data with null values.

MODELING THE DATA

Before proceding, we needed to decide how we wanted to gauge this data so that we could come up with meaningful results about them. Our group split up to explore different angles from which to analyze it.

The most obvious course of action to me would be to track the average scores of participant based on how frequently they would check social media. To do this, we sorted our dataframe based on participant ID and calculated the average gap in between each session, converting the timestamps into seconds. The subsequent graphs were scatter plots with average minutes between notifications as the x-axis and average score as the y-axis.

Another consideration I had was the impact of lurking variables such as traumatic news stories on the average scores each participant got. As this data was recorded from March to May of 2017, the Ariana Grande concert bombing occured while the experiment was still being conducted. Thus, I decided to produce a separate set of graphs contrasting the average scores of participants on 5/22/2017 (the day of the Manchester Bombing) versus all other days. To ensure unbiased results, I filtered out any participants who did not have any scores recorded on 5/22/2017. Afterwards, I created a multi-column bar graph comparing overall averages for each score. I found that the Stress and Concentration averages, in particular, were markedly higher on 5/22/2017 than other days, while all other emotions had little difference. Subsequently, I designed linear regression models plotting the average Stress and Concentration scores by average number of seconds per notification, with one line representing 5/22/2017 and the other representing all other days.

CONCLUSIONS

After producing several linear regression and bar models from this data, I found that there was extremely little correlation between social media usage frequency and severity of mood. Every single aggregate linear regression I yielded had an extremely low R value, meaning there was barely any correlation at all. Based on this, the frequency that somebody uses social media is not implied to have any drastic effect on their mood, and it is likely other factors are more influential.

Conversely, I found that traumatic news stories such as the Manchester Bombing do appear to yield more stress and concentration difficulty as a whole. Additionally, I found that those who receive notifications more frequently are likelier to have higher stress and lack of concentration scores; while the correlation is not very strong, it is at least more than the virtually nonexistent trend observed elsewhere.
