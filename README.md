This code allows you to scrape the basketball reference shooting page for midrange shots (10-16, and 16-3P range). 

I broke the code into 3 functions. The first scrapes the webpage. 

The second renames the columns to be (slightly...) more readable. The reason I did this is basketball reference labeled it an an unreadable way - for instance, shots from 3-10 feet were named %FGbydistance.2

the third function cleans up some remaining issues. First, it cuts any "holder" rows. Basketball reference has rows that are just repeating the column headers, 
since as a static html website, you can't have the column headers scroll down with the user. I deleted these rows

The other tricky thing is that if a player gets traded they are given another row in the dataframe with their new team. So the third function also sums the statistics by player

