## How Funding Disparities in U.S Public Schools Suggest Black/Hispanic Underrepresentation in High-Cost Sports
#### Is there a connection between income and sports partcipation opportunities?

### Introduction
Each year, the Aspen Institute releases the </i><i>State of Play</i> report, an analysis capturing sports participation data on youth in the United States. In the most recent report released in 2024, key findings suggest a connection between income and sports participation. 

According to the National Survey of Children's Health (NSCH), Vermont, Iowa, North Dakota, Wyoming, Maine, South Dakota, and New Hampshire reported the highest percentage of youth sports participation (over 63%). Alternatively, states such as New Mexico, Nevada, Mississippi, and Louisiana reported below average youth sports participation (under 54%). Excluding Nevada, the remaining states are among the poorest states in the country, and have larger minority populations -- while many of the states with the highest percentages have low minority populations. 

For instance, through data sourced from the Sports & Fitness Industry Association (SFIA) and their Sports Marketing Surveys (SMS), it was found that the sports particpation rate in Black youth aged 6-17 declined from 45% to 35% over a ten-year period (2013-2023).

It is important to note that sports participation rates in general have been steadily returning to how they were pre-COVID; however, the trends in youth sports participation post-COVID are shown differently among various demographics. For instance, youth aged 6-12 coming from lower-income families (under $25,000) were the only demographic that declined in sports participation rates from 2022 to 2023, while every other income bracket increased. 

### Purpose
Although more youth are returning to sports post-COVID, opportunities for sports participation seems to be heavily dependent upon various factors such as socioeconomic status, accesibility, and resource allocation. In public schools, disparities in funding can limit access to appropriate facilities, personnel, or physical education, which could hinder opportunities to participate in sports or physical activity. Outside of school, high-costs of specialized or club teams, or lack of accessibility to recreational facilities can also be barriers, especially for lower income families. 

#### Facility Quality 
In a 2021 report written by the 21st Century School Fund, a non-profit dedicated towards improving public school facilities, numerous inequities were found in public school funding due to racial, socioeconomic, and geographic factors. For example, rural school districts with lower-income public schools received about 2.3 million dollars per school to make capital improvements on facilities and buildings; however the average is 4.3 million dollars per school, meaning that those rural low-income schools were only receiving half as much as the national average. 

#### Physical Education
A study done by researchers for the Bridging the Gap program found that only 43% of students at Black public elementary schools received the recommended 20+ minutes of recess time, and 55% of students at predominately Hispanic/Latino schools. These percentages, when compared to the 77% of students at predominately White schools, suggest a correlation between race and disparities in physical activity offered to students through recess time. In another study conducted to examine physical activity among middle school students, researchers found a significant relationship between schools with a higher amount of students using the free/reduced lunch program and having less environmental access for physical activity. 

#### Specialized Sports
Many parents sign their children up for specialized sports -- year-round training and competition in the form of AAU or club teams -- in order to increase scouting opportunities and assist with skill/performance development. Sports specialization typically requires costly investments towards participation, travel, and equipment fees, which can create financial barriers, especially in high-cost sports such as tennis, gymnastics, and ice hockey.

### Methodology
<b>Public School Characteristics 2022-23<b>

Last Updated: October 21, 2024

https://catalog.data.gov/dataset/public-school-characteristics-2022-23-451db

The National Center for Education Statistics (NCES) gathers demographic and geographic data about U.S public schools and factors such as enrollment and Title I status. The variables that will be analyzed are those regarding free/reduced-price lunch (FRPL) rates, class size, and student demographics. 

The uncleaned dataset had 101,390 rows of data, with 77 columns. The first step was to address any missing values in the dataset, specifically in the FRPL columns. As indicated in the description of this dataset online, these missing values are represented by a number of indicators: -1 indicates that data is missing, -2 or N indicates that data is not applicable, and  -9 indicates that data did not meet NCES data quality standards. Because these values were negative, rows with these negative values were dropped. 
The next step was to make sure all of the schools being analyzed were 1) operational, so schools that were reported as "School temporarily closed" or "School to be operational within two years" in the 'Status' column of the dataset were removed. Similarly, this analysis is focused on traditional schools, so schools in the "SchoolType" column reported as alternative, special education, or career and technical schools were also removed. Additionally, columns unecessary to the analysis such as administrative information -- StaffFTE, Phone, LEA Name, LEA ID, etc. were removed as well. Lastly, since this analysis is focused on K-12 students, the columns 'Adult Ed' and 'Grade 13' were removed. 

Descriptive statistics were then used to find key information about the variables being analyzed such as minimum and maximum values, mean and median, quartile ranges, and standard deviation.

For visualizations, scatter plots and a bubble plot were chosen. These were chosen since because the main variables for analysis were both numerical and could be used to visualize any clear correlations between the two. Additionally, these visualizations were also color coded based on the predominant race (either Black, Hispanic/Latino, or White) of each school. Four scatterplots were generated; one with all of the races, and one for each of the races being analyzed. One bubble plot was generated using a sample size of 1000 schools which consisted of all analyzed races in one plot. 

### Analysis
According to the National Center for Education Statistics (NCES), the following percentages are used to determine low-poverty and high-poverty schools: 

- Low-poverty: 25% or less of students are FRPL eligible
- Mid-low poverty: 25.1% to 50% of students are FRPL eligible
- Mid-high povety: 50.1% to 75% of students are FRPL eligible
- High-Poverty: 75% or more of students are FRPL eligible

For the analysis, FRPL values were used as an indicator of income, while student-to-teacher ratio was used as an indicator of resource allocation. Further research might find that school locale (urban, suburban, town, rural) could also be factors that correlate with these variables, but they were not considered for this analysis. 

#### FRPL
The first observations are the mean values for students receiving free lunch, and those receiving reduced lunch. The mean value of students receiving free lunch is around 294.01 students, while reduced is around 35.52 students. Because significantly more students qualifying for FRPL are in need of the full free lunch on average, this could be a possible indicator of a lower-income school. The standard deviation (std) for the free lunch column is lower than the mean, while the std for the reduced price lunch column is higher, suggesting more variability in the number of students receiving reduced lunch. This is confirmed when looking at the quartile ranges; from 25% to 75% (5-45 students), the values suggest that while not many students recieve reduced-price lunch per school, some schools have up to 1400 students receiving it, which is higher than average. Through these statistics, it can be inferred that there are a small amount of schools that have a disproportionate amount of students receiving FRPL, and they might be overlooked if just looking at the mean itself. 

#### Enrollment Trends
The mean values for enrollment show a clear drop in enrollment from grade 9 to 12, starting at a mean of around 223.76 students (grade 9) per school to a mean of around 191.25 students (grade 12) per school. Grade 9 has a larger std than the mean, with a max value of 6251 students. Grade 12 also has a larger std than the mean, but there is only a .6 difference. 

#### Class Size
By looking at the descriptive statistics for the student-to-teacher ratio, the values seem consistent, as the std at around 13.33 students/teacher is lower than the mean of around 17.14 students/teacher. The 25%-75% ranges are also consistent (13.49-20.00); however, the max value is 1860 students/teacher, indicating either an errror in the data that was entered or an atypical class size.  

#### Race/Ethnicity of Students
The mean for total black students is around 89.30 students per school, yet the quartile ranges from 3-106 students; however, the max value goes up to 4402. For Hispanic/Latino students, the mean is around 177.29 students, with quartile ranges from 22-233; the max value goes up to 4065. The mean for white students is around 236.78 students, with quartile ranges from 50 to 332 students and a max value of 4294. These statistics suggest that white students are more evenly dispersed in schools, while Black and Hispanic students vary -- most schools have little to no Black or Hispanic students, while very few have high concentrations of them. 

### Visualization Findings

#### Scatter Plots
In the scatter plot displaying all races in this analysis (Black, Hispanic, white), the first item is that the number of points representing predominately white schools is signifcantly larger than the predominately Black or Hispanic schools. 

For predominately white schools, there is a larger concentration of points to the left (lower FRPL percentage). As the FRPL percentage increases, the number of students per teacher slightly decreases, but the plot itself does not show any extreme trends.

For predominately Black schools, there are significantly less points than the predominately Hispanic or white schools. On this plot, there is a much larger concentration of schools with a higher FRPL percentage, with most falling into 60-100%, and a very small amount of these schools that only have 0-40% of students eligible for FRPL.

For predominately Hispanic schools, there is also a larger concentration of schools having a larger FRPL percentage, though the points are more dispersed across the plot than those in the predominately Black schools plot. 

#### Bubble Plot
The bubble plot uses a sample size of 1000 schools and displays color-coded points to show if a school is predominately white, Black or Hispanic. This plot shows similar findings to the scatter plots; a higher concentration towards lower lunch rate percentages for predominately white schools, a dispersement of points (though more concentrated as the lunch rate increases) across the plot for predominately Hispanic schools, and a lack of predominately Black schools with points that trend towards higher lunch rate percentages. 

### Recommendations
Based on this analysis, key findings indicate inequities within the U.S public school system that could be improved through policy and intervention. The first is to make an effort to intentionally identify schools with a disproportinate amount of students receiving FRPL, rather than allow them to be overlooked by only considering mean values, especially when the data includes significant outliers. The second issue is the uneven dispersement of Black and Hispanic/Latino students in schools that highlights racial and socioeconomic issues. This could be addressed by identifying any barriers predominately Black or Hispanic schools might face, and by prioritizing resource allocation to schools with a large concentration of Black and Hispanic students in high poverty areas.

#### Conclusion
Though this research sought to explore how school funding and resource allocation could affect youth sports particpation, this analysis also highlighted broad racial and socioeconomic disparities in the U.S public school system. By using childrens' accessibility and opportunity for sports particpation as an example, the findings from this analysis point to a broader issue -- systemic inequities that can affect students' experiences and opportunities. To address these inequities, policymakers should be intentional and take notice of marginalized and underresourced communities to ensure all students and school districts from receive equitable opportunity and treatment. 

#### References
Aspen Institute. (2023). State of Play 2023. Project Play. https://projectplay.org/state-of-play-2023/participation 

Carlson, J. A., Mignano, A. M., Norman, G. J., McKenzie, T. L., Kerr, J., Arredondo, E. M., Madanat, H., Cain, K. L., Elder, J. P., Saelens, B. E., & Sallis, J. F. (2014). Socioeconomic disparities in elementary school practices and children's physical activity during school. American journal of health promotion : AJHP, 28(3 Suppl), S47–S53. https://doi.org/10.4278/ajhp.130430-QUAN-206

Young, D. R., Felton, G. M., Grieser, M., Elder, J. P., Johnson, C., Lee, J. S., & Kubik, M. Y. (2007). Policies and opportunities for physical activity in middle school environments. The Journal of school health, 77(1), 41–47. https://doi.org/10.1111/j.1746-1561.2007.00161.x
