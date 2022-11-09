# OWiT WhatsApp GC Analysis (AUG - OCT 2022)
Data cleaning, analysis and report creation for a  WhatsApp group chat data in PowerBI


# Introduction
I collected data from OWiT, a WhatsApp group and analyzed it to identify patterns and individual activities. OWiT is a study and accountability group (community) for women interested in joining the technology sector.

This project was one that resulted from boredom caused by sickness that would involve working with data that was personal and which the insights would be interesting to see. This documentation includes:
* Data Collection
* Data Cleaning & Transformation
* Report Requirement
* Report Design
* Data & Report Limitation
* Findings
* Conclusion


# Data Gathering
To obtain this data, I had to export the chat and to do this, I went to group chat, clicked on the More option(…) at the header, and clicked on ‘More’ then ‘Export Chat’. You can decide to export with or without media. In my case, I exported without media.
Here’s a link to guide you in [exporting WhatsApp chats](https://www.indiatoday.in/information/story/how-to-export-whatsapp-chats-1723409-2020-09-19).
The chat is exported as a text file. This was my first time analyzing a text file and I encountered some great surprises.



# Data Cleaning & Transformation
The exported chat was imported into Jupyter Notebook using pandas. There were various transformation methods I tried and I eventually stumbled on one by [rajkrishna92](https://github.com/rajkrishna92) that did exactly what I wanted so I took the parts of the code I needed and replicated for my own use. 
After obtaining clean data, I saved it as a csv file. Since I wanted to show how many admins were in the group chat, I had to create another table from the original and clean to meet the conditions necessary to become an admin. An admin had the power to add, remove or make someone else admin. So, I selected messages where those conditions were met to obtain an admin table.
Also, there were instances of "Media Omitted" in the message column which shows that a media was supposed to be there. SO, I counted those instances to know how many media files existed in the chat.
I cannot share the complete data cleaning file due to privacy reasons but these steps below would help you to atleast have a clean data in the dataframe format by following the stpes taken in the 'clean data' file.



# Report Requirement
While planning for this project the initial purpose of creating the report was to see the overall trend of conversations on the group and identify what period of time the most conversations took place. However, during the report design I was also interested in showing the following:
Number of messages sent
Media shared
Number of admins
Number of participants on the group
Most active participants by time, day, etc.


# Report Design
The layout for this report was created using Figma, a design tool that enables you to create designs for mobile and web interfaces as well as any other kind of design you can think of. After choosing the queries to be answered and the reports to use, several card designs were created for each viz and integrated into a single design. I used green because it speaks growth and at the same time is a popular trademark for WhatsApp. The Figma icon plugin iconify is where all of the icons used in this report were acquired from. Color schemes and shades were selected from adobe.color.com. You can access all necessary images and icons here.


Here is what the initial background for the dashboard looks like:
![owit analysis bg](https://user-images.githubusercontent.com/112688755/200859317-87db4e53-c1b9-4249-9a03-c83ef9bf8356.png)


And here is what the final combined report design looks like:
![Screenshot_20221109-154837_Chrome](https://user-images.githubusercontent.com/112688755/200862014-5a056675-0587-4cc6-b99d-58d51e9b7ab1.jpg)




# Data & Report Limitation
* From the data there is no way to identify who a message was responding to except the person was directly tagged.
* The data transformation and report does not provide data on who a message was in response to.


# Findings
* There were a totl of 26 members and just one admin in the group chat within the 3 months analysis. 
* There were a total of 8,645 messages and 1,110 media files sent on the group chat.
* Conversations were at a peak around 9pm and according to finding, this is the time for meetings whihc take place on Fridays and Sundays.
* There was a larer percentage of conversations recorded in August compared to Septmenber and October. 
* The most active participants are: Oluwatoni, Imisioluwa, Oyin, Daniella and Fisayo.

# Conclusion
It was enjoyable to work on this project. The Python script and documentation should make it easier for you to replicate using your own data. The process of data cleaning and data visualization as a whole may be improved in the future.

For privacy considerations, I didn't give access to the.pbix and whatsapp data. To see the complete functionality and User Experience, you may examine the [interactive version of the report](https://app.powerbi.com/view?r=eyJrIjoiYjQzYzk3NzQtMTc0NC00YWIxLWEzNjUtMDcxYTljNzA3MjhlIiwidCI6ImYxMDIxMjliLTQwMjUtNDFlOC05ZDAyLThlMzRmNmE1ZjQyNCJ9&pageName=ReportSectionb8fe89bf74b645d0e0cd).
