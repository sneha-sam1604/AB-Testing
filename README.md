# Email Campaign Data Analysis

## Introduction
This project analyzes the effectiveness of various factors on email campaign click rates using a dataset of email campaigns. The dataset includes information on whether the email contained discounts, personalization, images, and other features, as well as the time of day and day of the week the email was sent.

## Dataset
The dataset, named email_campaign_dataset.csv, includes the following columns:

campaign_id: Unique identifier for each campaign.
sender: Identifier for the sender of the campaign.
subject_len: Length of the email subject.
body_len: Length of the email body.
mean_paragraph_len: Average length of paragraphs in the email body.
day_of_week: Day of the week the email was sent.
is_weekend: Indicates if the email was sent on a weekend (1) or not (0).
times_of_day: Time of day the email was sent (e.g., Morning, Noon, Evening).
category: Category of the email campaign.
product: Product associated with the campaign.
no_of_CTA: Number of Call-To-Actions (CTAs) in the email.
mean_CTA_len: Average length of CTAs.
is_image: Indicates if the email contains images.
is_personalised: Indicates if the email is personalized (1) or not (0).
is_quote: Indicates if the email contains quotes.
is_timer: Indicates if the email contains a timer.
is_emoticons: Indicates if the email contains emoticons.
is_discount: Indicates if the email offers a discount (1) or not (0).
is_price: Indicates if the email mentions a price.
is_urgency: Indicates if the email conveys urgency.
target_audience: Target audience identifier.
click_rate: Click rate for the email campaign.

## Data Analysis
1. Click Rate vs. is_weekend
Welch Two Sample t-test Results
t = -4.2272
df = 488.24
p-value = 2.825e-05
95 percent confidence interval: -0.03521475 to -0.01286646
mean in group 0 (Weekdays) = 0.03708708
mean in group 1 (Weekends) = 0.06112769
Conclusion: Emails sent on weekends tend to have higher click rates compared to those sent on weekdays.

2. Click Rate vs. is_personalised
Welch Two Sample t-test Results
t = -1.2945
df = 116.39
p-value = 0.1981
95 percent confidence interval: -0.030331960 to 0.006354349
mean in group 0 (Non-personalized) = 0.04120811
mean in group 1 (Personalized) = 0.05319692
Conclusion: Personalizing emails does not significantly affect the click rates.

3. Click Rate vs. times_of_day
ANOVA Test Results
Df = 2
Sum Sq = 0.351
Mean Sq = 0.17567
F value = 25.41
p-value = 1.3e-11
Conclusion: The time of day has a significant effect on click rates, with Morning having the highest click rates, followed by Noon, and then Evening.

Tukey's HSD Test Results
Morning vs. Evening: diff = 0.04613180, p adj = 0.0000000
Noon vs. Evening: diff = 0.02193865, p adj = 0.0000046
Noon vs. Morning: diff = -0.02419314, p adj = 0.0116831
Conclusion: Morning click rates are significantly higher than Evening click rates. Noon click rates are significantly higher than Evening click rates. Noon click rates are significantly lower than Morning click rates.

4. Click Rate vs. is_discount
Welch Two Sample t-test Results
t = 17.819
df = 1844.9
p-value < 2.2e-16
95 percent confidence interval: 0.03303476 to 0.04120625
mean in group 0 (No Discount) = 0.043362161
mean in group 1 (Discount) = 0.006241661
Conclusion: Emails offering discounts have significantly lower click rates compared to those that do not offer discounts.

Repository Contents
email_campaign_dataset.csv: The dataset used for analysis.
analysis.R: R script containing the code for data analysis and statistical tests.

## Conclusion
This analysis provides insights into the factors that influence email campaign click rates. By understanding the impact of different variables, we can optimize email campaigns to achieve higher engagement.
