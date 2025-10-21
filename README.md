Algorithmic Admissions Activity

Inspired by: Survival of the Best Fit
Student: Lucas Montoya
Institution: Springfield University (Simulation)

Overview

This project explores how algorithms can influence fairness and equity in college admissions. Acting as an admissions committee member at Springfield University, I designed and tested an admissions algorithm that balances efficiency (academic performance) and fairness (contextual or social background).

Two models were developed:

Blind Model – evaluates applicants purely on academic and performance-based factors.

Aware Model – includes additional social context (income, first-generation status, legacy, disability, local status) to promote fairness and access.

The experiment shows how small adjustments to feature weights can significantly change outcomes for real applicants.

Files

Applicant.java – Defines the data model for each applicant (GPA, test score, extracurriculars, essay, recommendations, etc.).

Admissions.java – Contains the scoring logic (main file edited).

Main.java – Reads applicant data from applicants.csv and displays the admission results for both models.

applicants.csv – Dataset of fictional applicants.

README.md – Documentation, analysis, and reflection (this file).

Part 1: Implementing the Admissions Algorithm
Feature Weights & Design Choices
Blind Model

I used a straightforward merit-based formula that prioritizes academic metrics and performance-related factors.

Feature Weight
GPA 40%
Test Scores 30%
Extracurriculars  10%
Essay 10%
Recommendations 10%

This model excludes contextual data such as income, legacy, or geographic proximity. It evaluates every applicant "on paper" without social considerations.

Aware Model

The Aware Model introduces contextual fairness by giving boosts to applicants who face systemic barriers or have unique advantages.

Factor  Bonus
Low Income (< $40,000)  +10%
First-Generation College Student  +5%
Disability  +5%
Legacy Status +10%
Local Residency +5%

These adjustments are layered on top of the blind model’s score to acknowledge both potential and context. Legacy is included because some universities still weigh family history as part of tradition, while low income and first-generation bonuses aim to improve access for disadvantaged applicants.

Results Comparison
Applicant Blind Score Blind Result  Aware Score Aware Result  Outcome Change
Alice Stark 0.91  Admitted  1.00  Admitted  No change
Bob Parker  0.90  Admitted  1.00  Admitted  No change
Carlos Rivera 0.72  Rejected  0.87  Admitted  +Admitted
Diana Chen  0.91  Admitted  0.96  Admitted  No change
Fatima Al-Sayed 0.69  Rejected  0.89  Admitted  +Admitted
George Johnson  0.71  Rejected  0.86  Admitted  +Admitted
Hannah Miller 0.67  Rejected  0.77  Rejected  No change
Ishaan Singh  0.85  Admitted  0.90  Admitted  No change
Jasmine Okafor  0.73  Rejected  0.93  Admitted  +Admitted
Liam Wang 0.84  Admitted  0.94  Admitted  No change
Observations

The aware model admitted four additional applicants (Carlos Rivera, Fatima Al-Sayed, George Johnson, and Jasmine Okafor) who were previously rejected under the blind model.

These applicants likely benefited from low income, first-generation, or local-status boosts — showing that contextual awareness increases inclusivity without drastically penalizing academic strength.

Part 2: Discussion & Reflection
Feature Selection & Design

I chose to include GPA, test scores, extracurriculars, essays, and recommendations as the core quantitative measures. For the Aware Model, I added income, first-generation status, disability, legacy, and proximity to balance equity and tradition.

I did not exclude legacy because I wanted to show how both privilege (legacy) and adversity (low income) can coexist within an algorithm, creating an interesting tension between fairness and tradition.

If I expanded this model, I would consider adding essay sentiment analysis or volunteer service hours as additional factors of character evaluation.

Fairness & Outcomes

The Aware Model clearly benefited applicants with disadvantaged backgrounds:

Carlos Rivera, Fatima Al-Sayed, and George Johnson were likely low-income or first-gen students.

Jasmine Okafor may have been a first-gen or local student.

This shift made the admissions process more inclusive, though the added legacy advantage also benefited already privileged students.

Adding income and first-generation factors makes the system more fair by addressing barriers beyond academics. However, fairness is not perfect—boosting legacy also introduces bias in the opposite direction.

Overall, the aware model feels more balanced, recognizing potential and context rather than just numbers.

Transparency & Accountability

The algorithm is fairly transparent because each factor’s influence is clearly defined and adjustable. I could easily explain to an applicant why they were admitted or not (e.g., “your GPA and essay were strong, but your overall score did not meet the threshold”).

However, explaining “contextual boosts” might be controversial. Applicants might question why one person received a 10% boost for income while another didn’t.

I would feel somewhat comfortable being evaluated by this algorithm because it attempts to be fair, but I’d still prefer a human element to capture qualities numbers can’t.

Broader Implications

This simulation parallels real-world systems like:

Hiring algorithms (resume screening).

Loan or credit scoring models (socioeconomic bias).

Scholarship decisions (merit vs need).

It shows that algorithms reflect human priorities—they can’t eliminate bias, only shift where it appears.

If such a system were used in real admissions, the main risks would be:

Over-reliance on numerical thresholds.

Hidden bias in “neutral” variables (e.g., zip code correlating with income).

Lack of transparency in how weights are chosen.

True fairness in algorithms requires constant auditing, openness, and human oversight.

Conclusion

This project demonstrated that fairness in automated decision-making is subjective and context-dependent. By slightly increasing boosts for low-income, first-gen, and legacy applicants, I made the system more inclusive — but not perfectly unbiased.

Algorithms can help create efficiency and consistency, but ethical fairness requires human responsibility to interpret, justify, and continuously refine them.