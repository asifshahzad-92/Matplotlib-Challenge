# Matplotlib-Challenge
Data Analytics Challenge
_____________________________________
# Pymaceuticals Inc.
---

## Analysis

### Data Overview:

    1. Total *249* mice in the study.

    ![image](https://github.com/user-attachments/assets/4debed8a-3b36-4eba-9ae0-b7953d527ba0)


    2. Mouse ID (g989) was found to be duplicate; so, it was removed.
    
    3. After removing the duplicate, 248 unique mice remained in the study.

    

## Drug Regimen Comparison:

### Statistical Analysis:

    Capomulin and Ramicane showed the lowest mean tumor volumes (40.68 mm³ and 40.22 mm³ respectively).
    These two drugs also had the smallest variance and standard error, suggesting consistent performance.
    Ketapril had the highest mean tumor volume (55.24 mm³) and the largest variance, indicating less consistent results.

### Treatment Distribution:

Capomulin was the most frequently used treatment with 230 timepoints, followed closely by Ramicane with 228.
Propriva had the least number of timepoints at 148.

### Gender Distribution:
The study had a nearly even split between male (125) and female (123) mice.

### Outlier Analysis:

Infubinol was the only treatment that showed an outlier, with one tumor volume measurement of 36.32 mm³.
Other treatments did not show any outliers in their final tumor volumes.

### Capomulin Treatment Analysis:
For mouse l509 treated with Capomulin, tumor volume initially increased from 45.00 mm³ to 48.07 mm³ over the first 20 timepoints.
After timepoint 20, the tumor volume decreased, ending at 41.48 mm³ at timepoint 45.
This suggests Capomulin may have started to take effect after 20 timepoints.

### Correlation Analysis:
There is a strong positive correlation between mouse weight and average tumor volume for Capomulin (0.84) and Ramicane (0.81) treatments.
Ceftamin showed a very weak negative correlation (-0.04) between weight and tumor volume.
Overall, there was a weak negative correlation (-0.06) between mouse weight and average tumor volume across all treatments.
