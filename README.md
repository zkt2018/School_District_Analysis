#**School_District_Analysis**
##**Overview of the analysis**
In this project, we used Python to analyze the datasets of the City School district to evaluate the reliability of the data collected from different schools. Through this project, there were multiple school datasets available which required to be cleaned, sorted and organized in order to provide reliable results. Using Python Pandas and Numpy libraries, we evaluated the data from different aspects. The school board specifically requires the reliability of the Reading and Math scores from one of the schools. Hence, we analyzed data through both including and excluding Thomas High School dataset from the principal datasets.

##**Results**
After replacing the Thomas High School Ninth graders by NaN, the statistics of the district summary slightly changed. The images below demonstrate the district summary once with 9th graders and without 9th graders of Thomas High School.

*The initial District Summary:*

![district_sum_df_init.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/district_sum_df_init.png)

*District Summary after replacing Thomas High School’s 9th Graders with Nan:*

![district_sum_df.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/district_sum_df.png)

As the 9th graders' math and reading scores are only replaced, the number of students is still the same, and we see just a very slight improvement in the percentages. To actually exclude the impact of 9th graders, I recreated the data frame using the new total student numbers. The result shows that the total number of students without 9th graders is 38709 (vs. 39170) and the Passing Math, Reading and Overall percentages improve slightly more.

![district_sum_df_wo_nineth.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/district_sum_df_wo_nineth.png)

*Per School District Summary after replacing Thomas High School’s 9th Graders with Nan:*

![ths_tenth_twelfth_perc.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/ths_tenth_twelfth_perc.png)

The ninth graders are replaced by NaN values in the dataset to enable us to assess its impact on the statistics. The replacement impacted the scores of Thomas High School in all three categories. The percentages increased from 66.91, 69.66, and 65.08 percent for the three categories of Math, Reading, and Overall respectively, to 88.98, 93.66, 84.63 percent. With this increase, the school got the second top position in terms of performance.
The comparison of schools’ ranking based on the budget per student demonstrates the lower the budget, the higher the performance.

![ths_spending.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/ths_spending.png)

The scores by school size shows the larger schools, where the number of students is between 2000 and 5000, have a lower overall passing percentage than the other two groups. Among the other two groups, small and medium, the medium group (1000 to 2000) had the highest score and just less than %1 over the small group (less than 1000 students). 

![scores_by_school_size.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/scores_by_school_size.png)

Categorizing the schools based on their type reveals that the *Charter* schools have a better performance than the *District* schools. The overall passing percentage is approximately *%37* higher for *Charter* schools.

![scores_by_school_type.png](https://github.com/zkt2018/School_District_Analysis/blob/main/Resources/scores_by_school_type.png)

##**Summary**
Replacing the ninth graders, except for the school’s performance among the other schools within the district, does not significantly impact the statistics in Math and Reading scores by grade, school spending, size and type. As the number of students' grades omitted was less than 500 from the total of 39170. Hence, although this number could play a great role in one school’s statistics and move its position to the second top school, overall, it did not result in a great discrepancy on the other statistics of the whole district. Therefore, it is impossible to determine the accuracy of the data provided according to this analysis.
