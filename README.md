# School_District_Analysis
-----------------------------
## Project Overview

The purpose of this analysis was to assist a client named "Maria" in analyzing data on student funding and standardized test scores for a district of fifteen schools to determine what affects replacing ninth-grade math and reading scores for "Thomas High School" with "NaN" values would have on the district-wide analysis.  The motivation for this replacement procedure was to protect the district-wide analysis from potential misrepresentation, considering the ninth-grade students of "Thomas High School" had been suspected of academic dishonesty on their test scores.

To perform the analysis, a variety of metrics were calculated and analyzed for each school prior to the data manipulation experiment.  These included the total number of students, the total budget, the average math scores, average reading scores, the percentage of students that passed math, the percentage of students that passed reading, the percentage of students that passed both math and reading, and the percentage of students who passed overall.  Following this initial analysis, the "Thomas High School" student test scores for math and reading of ninth-graders were replaced with "NaN" values and the same analysis was performed to measure and compare the updated metrics results against the original metrics results.

----------------------------
## Resources

Data Sources:  schools_complete.csv, students_complete.csv

Software:  Python 3.8.3, Visual Studio Code 1.49.2

----------------------------
## Results

### District Summary Affects:

- The affect on the district summary is demonstrated by the following two dataframes.  The first dataframe represents the original summaries of all the district-wide metrics.  The second dataframce represents the summarized metrics following the inclusion of NaN values.  As you can see, the NaN values caused the average math score to drop .1 points, the average reading score to remain the same, the percent passing math to drop by .2, the percent passing reading to drop by .3 and the percent overall passing to drop by .1 point.
 
     ![](Resources/district_summary_df_originalone.png)

    ![](Resources/district_summary_df_new_with%20NaNs.png)

### School Summary Affects:

The following image shows the "tail-end" of the school summary dataframe prior to the replacement of ninth-grade data with NaN values:

   ![](Resources/school_summary_df_original.png)

- When the DataFrame included the rows for the 9th graders but their test scores were replaced with NaN values, their percentages for reading, math, and overall passing were in the range of the 60s.  This is because the total students in the data remained at 39,170 for this calculation, just as before the NaN values were introduced, but their values were no longer counted, resulting in a much lower percentage.  This can be seen by the following dataframe screenshot:

    ![](Resources/school_sum_NAN_60.png)


-From this dataframe, in comparison to the original, it is clear the data for Thomas High School test score percentages experienced a drastic reduction as a result of the NaN values.  Although the average math and reading scores remained relatively unchanged, the percent passing math decreased by about 26%, the percent passing reading decreased by 28%, and the overall passing percentage decreased by about 26%.

-However, this DataFrame did not adequately represent the rest of the students for Thomas High School.  Hence, a new dataframe was also created for Thomas High School to only include 10th, 11th, and 12th graders.  Once this dataframe was updated to more adequately represent the other grade scores of Thomas High School, the following results were obtained:
   
   ![](Resources/Use_for_NAN.png)

-By comparing this result to the original dataframe, the average math score and average reading score remained relatively unchanged.  The percentage math dropped just about .1 point, the percent reading dropped about 0.3, and the percent overall dropped about 0.3 as well.

- Thus, by replacing Thomas High School's math and reading scores with NaN values for ninth-graders, it appears this had the affect of reducing the scores for Thomas High School percentage performance results while leaving the rest of the school data intact.  However, once a new dataframe was created to only include data for the tenth, eleventh, and twefth grade students of Thomas High School, the percentages were recalibrated and became more similar to the rest of the district-wide data.

--------------------------

## Summary

As a result of the comparative data analysis, the replacement of ninth-grade test scores for "Thomas High School" with NaN values certainly altered the district-wide metrics results.  After reading and math scores for the ninth grade at Thomas High School were replaced with NaNs, major changes may be identified. 

Since there were only 461 NaN values replaced in the dataset out of 39,170 total students, the averages and percentages remained relatively representative of the district-wide metrics even after the second analysis.  Thus, it appears the results of the replacement of 461 potentially misrepresentative values with NaN values served well to succesfully safeguarded the datasets from potential misrepresentation, so long as the 9th graders of Thomas High School are not included in the results to skew the percentages.  Of course, this was in imperfect solution, but it was a succesful resolution nonetheless.
