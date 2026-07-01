# Creative Challenge: Extracting Insights from Banking Customer Feedback for Churn Reduction

This repository contains the resolution for the Creative Challenge, applying Data Science and Business Intelligence (BI) concepts to transform banking customer feedback into proactive retention strategies.

---

## 🧱 Step 1: Define the Intention

* **I want the AI to analyze** a dataset of comments, complaints, and feedback from digital banking channels **to identify** behavioral patterns, operational bottlenecks, and dissatisfaction signals that indicate an imminent risk of churn (customer attrition).
* **The result will be used by** Business Intelligence (BI) and Customer Success (CS) teams **to support** decision-making in proactive retention campaigns, quick fixes in the user journey, and mobile app usability improvements.
* **The output must contain** a structured markdown table categorized by churn risk level (High, Medium, Low), the most frequent friction points, and actionable recommendations for preventive measures.
* **The result will be considered successful if** it delivers highly actionable and predictive insights (focused on preventing customer loss before it happens), is clearly organized, and distinguishes operational pain points (technical app errors) from financial/service pain points (fees and customer support issues).

---

## 🧱 Step 2: Add Context and Restrictions

* **Context:** I am working with retail banking customer feedback related to the mobile app, instant payments (Pix), investments, and digital support channels (chat and WhatsApp). The bank's primary goal is to lower the quarterly churn rate.
* **Available Data:** The simulated dataset contains the following columns: `Customer_ID`, `Comment_Date`, `Source_Channel`, `Feedback_Text`, `Product_Mentioned`, `Account_Balance`, and `Engagement_Score (1 to 10)`.
* **Analysis Criteria:** The AI must classify the feedback by crossing three pillars: **Theme** (e.g., payment failure, unfair fees, support delay), **Sentiment** (Negative, Neutral, Positive), and **Churn Risk** (calculated by combining the severity of the complaint with low engagement scores or low account balances).
* **Guardrails and Restrictions:**
  * Rely strictly on the provided dataset without assuming or inventing external scenarios.
  * Do not fabricate fake metrics, statistics, or root causes unsupported by textual evidence in the comments.
  * Protect privacy: ensure that any personally identifiable information (PII) or sensitive customer data is completely ignored or masked by the AI.
  * If the data is insufficient to determine the risk level for a specific category, explicitly state this limitation.
  * Maintain an executive, analytical, technical tone fully geared toward strategic business decision-making.

---

## 🚀 Step 3: The Final Refined Prompt

```text
Act as a Senior Data Scientist specializing in Business Intelligence (BI) applied to Banking Customer Retention.

Your task is to analyze a dataset of customer comments and feedback regarding digital channels (mobile app, Pix, investments, and chat support) to identify users at high risk of churn.

Context: The bank has experienced a drop in active users over the past few months. This analysis will be used directly by the Business Intelligence Committee and the Customer Success leadership to trigger proactive retention campaigns and secure these accounts before final cancellation.

Available Data: You will be provided with a dataset containing the following columns: `Customer_ID`, `Comment_Date`, `Source_Channel`, `Feedback_Text`, `Product_Mentioned`, `Account_Balance`, and `Engagement_Score (1 to 10)`.

Analysis Instructions:
1. Classify the feedback by Main Theme (e.g., Technical Failure, Fees, Support), Sentiment (Positive, Neutral, Negative), and assign a Churn Risk category (High, Medium, Low). Risk must be classified as "High" if the sentiment is negative and the Engagement_Score is below 4.
2. Identify the top 3 most critical complaint patterns directly linked to severe financial or technical dissatisfaction.
3. Provide explicit evidence from the dataset, using short direct quotes from customers to validate each identified pattern.
4. Suggest at least 3 practical and immediate actions for the BI team to implement within the customer engagement and retention workflow.

Output Format:
- A macro Executive Summary (maximum of 5 lines) highlighting the overall diagnosis of the dataset.
- A structured Markdown Table with the columns: [Theme] | [Churn Risk Level] | [Customer Evidence/Quote] | [Recommended BI Action].
- A bulleted list highlighting the top 3 priorities that the product engineering or support teams must resolve to stem customer churn.

Absolute Restrictions:
- Restrict yourself strictly to the provided data; do not assume external behaviors or generate fictional data.
- Do not invent impact metrics that cannot be calculated directly from the shared text and numerical inputs.
- Adhere to data privacy best practices (LGPD/GDPR): ignore and remove any mention of sensitive data, names, tax IDs, or financial numbers accidentally exposed in the text.
- If data from a specific channel is scarce, declare this methodological limitation in the report.
- Adopt an executive, analytical, concise, and business-value-oriented communication tone.
