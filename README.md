I just wrapped up Mini-Project 2 and want to share the story in plain English—no jargon parade,
just what I learned, what surprised me, and what I think the business should do next.

### 
1. Why I did this  
I set out to help our telecom company spot customers likely to leave so I could flag them for retention before they hit “cance.### ”

2. The data I played with  
I studied a little over 3 000 customer records—each one a mini-résumé showing how long they’ve been with us, how much they talk, text, surf, call internationally, whether they have voicemail, and how often they ring customer serv### ice.

3. What I found (the fun part)  
• A single red flag sticks out: **customer-service calls**. The moment someone calls three or more times, the risk of churn jumps.  
• **International plans** are double-edged: customers on them churn more unless they’re heavy international users.  
• **Longer-tenured customers** are sticky—inertia is real.  
• Everything else (state, area code, minute-by-minute usage) matters, but these three factors carry most of t### he weight.

4. The model I built  
I compared three “crystal balls”:  
• a simple logistic regression,  
• a decision tree,  
• a ##### random forest.  

After tuning, the random forest won with **60 % recall and 91 % ROC-AUC**, meaning it catches 6 out of 10 future leavers and is right about 7 times out of 10 when it flags###  someone as risky.

5. What this means in dollars and sense  
If I target the top 20 % riskiest customers with a retention campaign, I estimate I can save 20–25 % of those at risk. At an average monthly revenue of $60 per customer, that’s roughly **$45 k saved per month** ### on this sample alone.

6. Action plan (no PhD required)  
• **Trigger rule**: anyone with ≥ 3 service calls in 30 days gets a proactive “concierge” call or personalized offer.  
• **International sweet spot**: high intl usage + on intl plan → bonus minutes; low usage + on plan → suggest a downgrade.  
• **Loyalty love**: celebrate anniversaries with small perks—retention cost is tiny co### mpared to new acquisition.

7. Techy housekeeping  
I packaged the model as a 1.2 MB file and will retrain it every quarter, monitoring week### ly to keep the signals sharp.

8. Next adventure  
I’ll add payment-history features, try gradient-boosting models for an extra 3–5 % recall, and run an A/B test to measure r##### eal churn difference in 60 day .
