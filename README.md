# Analysis-of-US-Presidents-Data-in-Python
This is analysis of a dataset of presidents of the United States conducted in Python. I did this for my course at Boston University, CS 677: Data Science in Python, in fall 2023.

Attached are charts, my code as an IPYNB notebook, and my code and output with conclusions in a report as a PDF.

The dataset is a tab-separated value text file (tsv) saved "erroneusly" (though deliberately as part of the assignment) as a .csv. I saved time on cleaning the data and preparing it for processing by discovering this (it was also in ANSI format rather than, say, UTF-8 or UTF-16). Some of my classmates unfortunately didn't realize this in their own code and dedicated extensive effort to cleaning the data with regex or NTLP tokenizers.

Further processing included removing all then-living presidents from the dataset.

The dataset itself contains biographical details on US presidents such as terms in office, education, career/trade prior to the presidency, and political affiliation.

I tabulated and visualized such data as party affiliation. The assignment required pie charts, though I will note that these are inefficient and not preferred as best practice in data analysis and data science for relaying this information:

![a pie chart of presidential party affiliation](https://raw.githubusercontent.com/GriffinLyons/Analysis-of-US-Presidents-Data-in-Python//main/pres_pie.png "Presidential Party Affiliation") 

I charted the age of presidents on entering office, and broke the data up by simplified political party ("Republican", "Democrat", and "Other"). To do this, I had to employ Python's re module on strings of each president's years in office to obtain their respective first years in office.

![a line chart of presidents' ages upon assuming office, by party affiliation](https://raw.githubusercontent.com/GriffinLyons/Analysis-of-US-Presidents-Data-in-Python//main/pres_line_chart.png "Presidents' Ages At Start of Term, By Party Affiliation") 

The dataset was neither comprehensive nor always accurate; more than 20 US presidents were trained or worked as lawyers, but only three were listed as such in trade or education.
