# School District Analysis

## Overview of the school district analysis: 
To analyze schools within the district for reading and math scores averages, percentage of students passing reading, math and both reading and math. To gather a school summary looking at the same data as well as spending per student. Last to see where the scores fall based on school spending, size and type to see if there might be a correlation between the scores and any of those variables, i.e., do schools who spend have higher passing percentages or perhaps is it smaller schools that have higher passing percentages, etc. Lastly, to adjust all prior analysis taking into account suspected academic dishonest at Thomas High School (THS) for 9th graders in both reading and math.

## Results
- Once the data was removed from THS 9th grade and replaced with NaN, and the student count adjusted to remove the number of 9th graders at THS the averages and percentages shifted slightly down. However, the shift was marginal less than 0.3% in all cases. See images below.

        The district summary with THS 9th grade scores:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/DistSummarywithTHS9th.png)
    
        The district summary without THS 9th grade scores:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/DistSummarywoTHS9th.png)
    
- At the school summary level, no changes were made to other school’s summary from the original analysis with the original data including THS 9th graders scores. However, THS had to be updated to exclude all 9th graders from the analysis as including all the NaNs disrupted the accuracy of the passing reading, math and both percentages as those numbers originally were calculated with the whole student count at THS. To make this adjustment for more accuracy I removed the 9th grade student count (461 students) from the overall THS student count (1635) to conduct the math on only students with score. As you can see below THS counting 461 students with no score significantly changes the summary compared with both data with the 9th graders scores and data without 9th graders score, though again the difference between with 9th grader scores and without 9th graders scores is marginal at less than 0.4% change in each area.

        THS with 9th graders NaN scores in count:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSwith9thnans.png)
    
        THS with 9th grader scores in tact:
    ![image]

        Every School Summary with adjusted THS numbers:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THS10thru12onlydata.png)

- Even with replacing 9th graders scores with NaN and removing their count from the calculations, thus only fining averages based on 10-12th grader scores Thomas High School remained in the top 5 schools, still in the number 2 slot but their lead over the number 3 school reduced from almost 0.04% to less than 0.01% in overall passing. However, had the 9th grade NaN scores been left in the account as show in the 'THS with 9th graders NaN score in count' above THS would have fallen out of the top 5 but still been higher performing the bottom 5.

        Top performing with THS 9th graders score:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/top5alldataused.png)
 
        Top performing after THS 9th graders scores removed:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/top5alldataused.png)

        Bottom performing (saw no change to the original analysis):
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/bottom5alldataused.png)

- Replacing the ninth-grade scores had the following affects:
    -Math and reading scores by grade: no effect on other schools, only THS changed from a 83.6 math score and 83.7 reading score to a nan in both categories for 9th graders, see second image below.
        
        Before with THS 9th graders score math and reading:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSmathscoresbygradewith9th.png)
    ![Image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/THSreadingscoresbygradewith9th.png)
    
        After without THS 9th graders score math and reading full summaries:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbygradesummarymath.png)
    ![Image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbygradesummaryreading.png)
 
   -Scores by school spending: no change from original analysis numbers probably because the change in scores was less than 0.04% without 9th graders vs with 9th graders so once broken down into spending per student there was no significant change, plus regardless of 9th graders not having schools THS would still spend the same amount on each of those students. 

        Scores by Spending Ranges:
     ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/spendingrangesperstudentwo9th.png)
 
   -Scores by school size: no change from original analysis numbers probably because the change in scores was less than 0.04% without 9th graders vs with 9th graders so once broken down into school size per student there was no significant change as THS would still fall into category Medium even without 9th grader count. 

        Scores by School Size:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbysizewo9th.png)
 
    -Scores by school type: no change from original analysis numbers probably because the change in scores was less than 0.04% without 9th graders vs with 9th graders so once broken down into school type the margin if not large enough to change the overall number for Charter schools which is what THS is.

        Scores by School Type:
    ![image](https://github.com/trosie3/School_District_Analysis/blob/main/Resources/scoresbyschooltypewo9th.png)

## Summary: 
By replacing THS 9th graders scores with NaNs there were 4 main changes to the analysis:
    1. Marginal change to the district summary overall reading, math and combines passing percentages
    2. Marginal change in THS school summary for reading, math and overall passing percentages
    3. Marginal change in top performing school scores for THS score but no change in ranks
    4. In breakdown of scores by grade there is now no data for 9th grade reading or math at THS.

These 4 changes can be looked at two ways. The first is relatively positive as it appears that even without the suspected academic dishonesty THS had little effect on the overall outcomes and scores to analyze, and appears to still be a top performing school. The second is it leads to questions on THS scores from other grades, as well as begging the question if we had accurate 9th grader schools for THS how would that affect the overall analysis. For example, if accurate scores show 9th graders at THS performing very poorly then the school as a whole would likely be brought down in performance and passing percentages perhaps even falling out of the top 5, or if other grades also had academic dishonesty there would likely be the same affect causing a further audit just into THS to fairly access their accurate numbers verses others schools who are not suspected of academic dishonesty. 

Using the data as it stands now, there are some trends we can identify:
    - Schools that spend less than $630 per student have higher passing rates
    - Large schools (more than 200 students) have the lowest passing rates, with medium having the highest followed very closely by small school.
    - Charter schools have higher passing rates than Regular district schools
To test those trends, we can look at the performance of schools and what we find is:
    - The top 5 schools are all charter schools, aside from one Wilson High School all are Medium or Small in size, and all aside from Thomas High Schools spend less than $630 per student.
    -The bottom 5 schools are all large schools, are all district schools and all spend more than $630 per student.
        - Perhaps to bring these schools up considerations should be made to split into more schools of less than 2000 students, and adjust budgets.
