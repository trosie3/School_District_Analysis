# School District Analysis

## Overview of the school district analysis: 
To analyze schools within the district for reading and math scores averages, percentage of students passing reading, math and both reading and math. To gather school summaries looking at the same data as well as spending per student. Next, to see where the scores fall based on school spending, size and type to see if there might be a correlation between the scores and any of those variables, i.e., do schools who spend more have higher passing percentages, or perhaps is it smaller schools that have higher passing percentages, etc. Lastly, to adjust all prior analysis taking into account suspected academic dishonesty at Thomas High School (THS) for 9th graders in both reading and math.

## Results
- Once the data was removed from THS 9th grade and replaced with NaN, and the student count adjusted to remove the number of 9th graders at THS, the averages and percentages shifted slightly down. However, the shift was marginal at less than 0.3% in all cases. 

     The district summary with THS 9th grade scores:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/DistSummarywithTHS9th.png)
    
     The district summary without THS 9th grade scores:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/DistSummarywoTHS9th.png)
    
- At the school summary level, no changes were made to other school’s summary from the original analysis with the original data including THS 9th graders scores. However, THS had to be updated to exclude all 9th graders from the analysis as including all the NaNs disrupted the accuracy of the passing reading, math and both percentages as those numbers originally were calculated with the whole student count at THS. To make this adjustment for more accuracy I removed the 9th grade student count (461 students) from the overall THS student count (1635) to conduct the math on only students with score. As you can see below THS counting 461 students with no score significantly changes the summary compared with both data with the 9th graders scores and data without 9th graders score, though again the difference between with 9th grader scores and without 9th graders scores is marginal at less than 0.4% change in each area.

     THS with 9th graders NaN scores in count:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSwith9thnans.png)
    
     THS with 9th grader scores in tact:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSwith9thintact.png)
   
     Every School Summary with adjusted THS numbers:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THS10thru12onlydata.png)

- Even with only using averages based on 10-12th grader scores, Thomas High School remained in the top 5 schools as number 2 but their lead over school number 3 school reduced from almost 0.04% ahead to less than 0.01% ahead in overall passing scores. However, had the 9th grade NaN scores been left in the account, as shown in the 'THS with 9th graders NaN score in count' above, THS would have fallen out of the top 5 but still been higher performing the bottom 5.

    Top performing with THS 9th graders score:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/top5alldataused.png)
    
    Top performing after THS 9th graders scores removed:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/top5cleandataused.png)
    
    Bottom performing (saw no change to the original analysis):
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/bottom5alldataused.png)

- Replacing the ninth-grade scores had the following affects:
    - Math and reading scores by grade: no effect on other schools, only THS changed from a 83.6 math score and 83.7 reading score to a nan in both categories for 9th graders, see second set of images below.

    Before with THS 9th graders score math and reading: 
    
     ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSmathscoresbygradewith9th.png)![Image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSreadingscoresbygradewith9th.png)
    
    After without THS 9th graders score math and reading full summaries:
    
     ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbygradesummarymath.png)![Image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbygradesummaryreading.png)
 
     - Scores by school spending, school size and school type: saw no change compared to original analysis numbers which included the THS 9th graders scores. This is because the change in score percentages was less than 0.04% at most without 9th graders. Size, type and school spending per student do not change for THS either. Thus, with only a marginal shift the new numbers were not significant enough to change the overall analysis for scores by school spending, scores by school size, or scores by school type.
    
    Scores by Spending Ranges:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/spendingrangesperstudentwo9th.png)
 
    Scores by School Size:
        ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbysizewo9th.png)
 
    Scores by School Type:
    
     ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbyschooltypewo9th.png)

## Summary: 
- Using the data as it stands now, there are some trends we can identify:
    - Schools that spend less than $630 per student have higher passing rates
    - Large schools (more than 200 students) have the lowest passing rates, with medium having the highest followed very closely by small school.
    - Charter schools have higher passing rates than Regular district schools

- To test those trends, we can look at the performance of schools and what we find is:
    - The top 5 schools are all charter schools, aside from one Wilson High School all are Medium or Small in size, and all aside from Thomas High Schools spend less than $630 per student.
    - The bottom 5 schools are all large schools, are all district schools and all spend more than $630 per student.
        -- Perhaps to bring these schools up considerations should be made to split into more schools of less than 2000 students, and adjust budgets.

### Limitations:
By replacing THS 9th graders scores with NaNs there were 4 main changes to the analysis:

   1. Marginal change to the district summary reading, math and overall passing percentages
   2. Marginal change in THS school summary for reading, math and overall passing percentages when data from 461 students excluded from calculations
   3. Marginal change in THS' score within the top performing school scores but no change in top 5 order
   4. In breakdown of scores by grade there is now no data for 9th grade reading or math at THS

These four changes can be looked at in two ways. The first is relatively positive as it appears that even without the suspected academic dishonesty, THS' new scores had little effect on the overall analysis, and THS appears to still be a top performing school. The second view is more skeptical, with one grade having academic dishonesty you have to wonder about THS scores from other grades, or what if we had accurate 9th grader scores for THS, how would either or both of those affect the overall analysis. 

If more time, gaining accurate scores 9th graders would solve this, or at least gaining scores from 9th graders scores that are accurate leading to less student scores being excluded from analysis. If we had those numbers, and those scores were poor then the school as a whole would likely be brought down in performance and passing percentages. It would also significantly change the analysis on the district summary and other areas using every school’s data in the calculation. Of course, it is also possible that the accurate scores would fall in line with the scores throughout the school, which would not significantly change the analysis. Another area that should be explored is the accuracy of other THS grade scores.

