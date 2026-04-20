---
editor: visual
---

# Data Source Description

For this project, you will use the 2024 wave of the [American National Election Studies](<https://electionstudies.org/>) (ANES). The ANES is conducted every two to four years to coincide with elections and surveys respondents about a variety of political beliefs and practices.

From the full data, I have extracted and recoded the following variables for our use as an analytical dataset. To load this dataset in R, you just need to run the setup code chunk in the full_report.qmd quarto document. The name of the dataset in R is `anes`.

-   **trust_government**: The trust in government variable is constructed from three separate variables that asked respondents for their level of trust in congress, the judiciary, and the government generally. For each question, respondents could respond that they "Trust a lot", "Trust somewhat", "Do not trust very much", and "Do not trust at all". Each of these categories was scored from zero to three, with higher values indicating more trust and then these were summed up across the three variables, leading to a single trust measure that is scored from zero to nine. This is the key dependent variable.
-   **media_trad**: Respondents were asked how many days a week they used the following news sources: broadcast TV, cable TV, radio, print newspaper. This variable takes the mean across all four variables and ranges from zero to seven days. Along with **media_online**, this is the key independent variable.
-   **media_online**: Respondents were asked how many days a week they used the following news sources: online news outlets, social media. This variable takes the mean across both variables and ranges from zero to seven days. Along with **media_trad**, this is the key independent variable.
-   **age**: The respondent's age in years.
-   **sex**: The sex of the respondent, recorded as male or female. This is the key contextual variable.
-   **educ**: The educational level of the respondent measured in five ordinal categories.
-   **party_affiliation**: The party affiliation of the respondent. Individuals were originally asked a seven point scale from Strong Democrat to Strong Republican, with Independent in the center. Independents how reported that they leaned in one party direction or another were included with that party for this variable.
