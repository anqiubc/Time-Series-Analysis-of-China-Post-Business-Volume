# Time-Series-Analysis-of-China-Post-Business-Volume
With R. Initial attempt in December, 2020.

## Summary
- Built a SARIMA model to fit the business volume data, which successfully detected the periodic pattern in the data, especially the seasonal peaks and valleys. 
- Predicted volume in 2020 using the model. Compared the predictions with the real data, fitted a quadratic model for this year, and analyzed the reason behind the fast growth during the COVID-19 period. 

## Dataset  
The dataset describes monthly postal delivery quantity (Unit: 10k), from November 2008 to October 2020, a total of 144 pieces of data in 12 years. I made the model used the data from November 2008 to October 2019 (132 entries), and used the data from November 2019 to October 2020 (last 12 entries) to evaluate my prediction with the model. Source: http://www.spb.gov.cn/ (State Post Bureau of The People's Republic of China)

## Target
- Courier quantity is an indicator that is closely related to many factors in life. Under the influence of large-scale online shopping promotions in China such as "Double Eleven"(11.11) and "Double Twelve"(12.12), the Spring Festival holiday, and students' winter and summer vacations, will there be periodic changes in the number of express delivery? 
- In addition to these relatively clear and direct influencing factors, the overall domestic environment at different times will inevitably have a certain impact on it. In particular, the sudden outbreak of COVID-19 in early 2020 still affects our lives to a certain extent today, and all industries have been impacted and affected. Under this special background, can our data also reflect some information about this special period from the side?   
- Therefore, The main problem that the analysis wants to explore is: **Whether the number of express delivery changes with time has a certain pattern?**

## Conclusion
- There is indeed a periodic pattern in the volume of postal express delivery. May is a small peak every year, November is a huge peak, and February may indeed be a valley due to the Spring Festival holiday. In addition, in the past ten years, the express delivery volume has shown a quadratic growth. After detrending, I fit a SARIMA model to the variance-stabilized transformed data, which nicely reflects this information in the process.  
- In addition, I also analyzed the fast growth of express delivery during the COVID-19 period, and consulted background materials to explore the reasons for its growth. The rapid growth of data in 2020 presents a non-linear quadratic form, showing that the postal express industry has undertaken relatively important work during the COVID epidemic. 