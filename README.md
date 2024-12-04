# Matplotlib-Challenge
Data Analytics Challenge
_____________________________________
# Pymaceuticals Inc.
---

## Analysis

### Data Overview:

1. **Total Mice in Study:**
    Total *249* mice in the study.

2. **Duplicate Mouse ID:**
    Mouse ID *(g989)* was found to be duplicate; so, it was removed.
    
4. **Total Mice under study:**
    After removing the duplicate, *248* unique mice remained in the study.

5. **Gender Distribution:**
    The study had a nearly even split between male *125* and female *123* mice.


## Drug Regimen Statistical Comparison:

**Mean, Variance, Standard Error Analysis:**

    1. Capomulin and Ramicane showed the lowest mean tumor volumes (40.68 cubic mm and 40.22 cubic mm respectively).
    2. Capomulin and Ramicane also had the smallest variance (24.95 cubic mm and 23.49 cubic mm)
    3. Standard error for Capomulin and Ramicane is lowest (0.33 cubic mm and 0.32 cubic mm), this suggest effective performance.
    3. Ketapril had the highest mean tumor volume (55.24 mm³) and the largest variance (68.55 cubic mm) and standard error (0.60 cubic mm), indicating lower effective results.

**Number of times Each Drug was used:**

Capomulin was the most frequently used treatment with 230 timepoints, followed closely by Ramicane with 228 while Propriva had the least number of timepoints at 148. 

    List of Number of times drugs used:
    
Drug Regimen:    Count
- Capomulin:     230
- Ramicane:      228
- Ketapril:      188
- Naftisol:      186
- Zoniferol:     182
- Stelasyn:      181
- Placebo:       181
- Infubinol:     178
- Ceftamin:      178
- Propriva:      148

**Outlier Analysis:**

    Infubinol was the only treatment that showed an outlier, with one tumor volume measurement of 36.32 mm³.

**Capomulin (Mouse id: l509) Treatment Analysis:**

    For mouse id l509 treated with Capomulin, tumor volume initially increased from 45 cubic mm to upto 48 cubic mm over the first 20 timepoints. However, after timepoint 20, the tumor volume decreased,       which shows the efficacy of Capomulin after 20th timpoint, ending at about 41 cubic mm.

**Correlation and Regression line Analysis:**

    1. According to Pearson correlation coefficient method there is a strong positive correlation between mouse weight and average tumor volume for Capomulin (0.84).
    2. Pearson correlation coefficient method for Ramicane also shows a strong correlation (0.81) between mouse weight and average tumor volume.
    3. Ceftamin Pearson correlation coefficient method showed a very weak negative correlation (-0.04) between weight and tumor volume.
    4. Infubinol shows a weak negative correlation (-0.06) between mouse weight and average tumor volume according to Pearson correlation coefficient method.
