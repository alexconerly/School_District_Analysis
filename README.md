# School_District_Analysis
-----------------------------
## Project Overview

The purpose of this analysis was to assist a client named "Maria" in analyzing data on student funding and standardized test scores for a district of fifteen schools to determine what affects replacing ninth-grade math and reading scores for "Thomas High School" with "NaN" values would have on the district-wide analysis.  The motivation for this replacement procedure was to protect the district-wide analysis from potential misrepresentation considering the ninth-grade students of "Thomas High School" had been suspected of academic dishonesty on their test scores.

To perform the analysis, a variety of metrics were calculated and analyzed for each school prior to the data manipulation experiment.  These included the total number of students, the total budget, the average math scores, average reading scores, the percentage of students that passed math, the percentage of students that passed reading, and the percentage of students that passed both math and reading.  Following this initial analysis, the "Thomas High School" student test scores for math and reading of ninth-graders were replaced with "NaN" values and the same analysis was performed to measure and compare the updated metrics results with the original metrics results.

----------------------------
## Resources

Data Sources:  schools_complete.csv, students_complete.csv
Software:  Python 3.8.3, Visual Studio Code 1.49.2

----------------------------
## Results

- The affect on the district summary is demonstrated by the following two dataframes.  The first dataframe represents the original summaries of all the district-wide metrics.  The second dataframce represents the summarized metrics following the inclusion of NaN values.  As you can see, the NaN values caused the averages and percentages of scores to decrease but by no more than a tenth of a percent in any categorical metric.
 
    ![](Resources/district_summary_df_original_but_to_one_decimal.png)

    ![](Resources/district_summary_df_new_with%20NaNs.png)

- The affect on the school summary is demonstrated by the following dataframes. The first DataFrame highlights a section of the the original school summary dataframe and the bottom DataFrame highlights a section of the updated school summary DataFrame which corresponds to the existence of NaN values.  As you can see by comparing the DataFrames, the average math and reading scores stayed relatively unchanged, the % passing math decreased by 26.4%, the % passing reading decreased by 27.6%.
The % overall passing decreased by 26.0%.
- 
----------------------------

![](Resources/school_summary_df_original.png)

![](Resources/school_summary_df_NaN.png)


- By replacing Thomas High School's math and reading scores with NaN values for ninth-graders, it appears this only really affected Thomas High School.

--------------------------

## Summary

As a result of the comparative data analysis, the replacement of ninth-grade test scores for "Thomas High School" with NaN values certainly altered the district-wide metrics results.  However, since there were only 461 NaN values replaced in the dataset out of 39,170 total students, the averages and percentages remained relatively representative of the district-wide metrics even after the second analysis.  Thus, it appears the results of the replacement of 461 potentially misrepresentative values with NaN values served well to succesfully safeguarded the datasets from potential misrepresentation.

Four major changes



One interesting observation includes the fact that even though the 9th-grate students of Thomas High School were suspected of academic dishonesty, apparently replacing their potentially erroneous test scores with NaN values actually increased the overall percentage of the overall metrics.  This suggests that even if many of these students manipulated the data to improve their reported scores, the overall scores of these students were still lower than the district-wide averages.  Thus, ridding the dataset from ninth-grade test reports increased the averages and percentages of the district-wide metrics overall.


Nevertheless, four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.