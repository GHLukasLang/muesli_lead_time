# Supply Chain Analysis: Improving Lead Time for a B2C Cereal Company

The client is a B2C cereal company selling solely through their online channels to customers, no physical stores. The project has two parts: First, check the stakeholder's assumptions and reconstruct the actual process that makes up the lead time. Second, make suggestions to improve lead time.

## Stakeholder's assumptions

According to the stakeholder:

- Step 1: orders take 3 days to process
- Step 2: when ready, they wait 1-2 days for a truck (trucks come on Mondays, Wednesdays and Fridays)
- Step 3: delivery takes another 3 days

Additionally, step 2 can be sped up if customers pay for express shipping. Express shipments are put on trucks as soon as they are ready. This gives us an average lead time of 7.4 in general, and 6 days for express orders.

## Results: 

### Average Lead Time is 57% higher than expected, with 11 days instead of 7

![Plot to visualize average lead time](viz/plot1.png)

Contrary to the stakeholder's assumption, the average lead time is 4 days higher than expected.

50% of all orders have a lead time of 9 to 13 days. Only 25% of orders have a lead time that conforms to the expectations.

![Boxplot to visualize interquartile range](viz/boxplot.png)

If we look at the individual steps, the analysis revealed:

- Step 1: processing takes on average 4 days, which is a day more than expected
- Step 2: when ready, orders wait on average 1.5 days, which conforms to the stakeholder's hypothesis
- Step 3: Delivery takes 4.5 days on average, which is 1.5 days longer than expected

### Express Shipping influences processing time

Express shipping influences the processing time **and** the pickup time, although the client's hypothesis was that it only effects pickup time.

Orders with express shipping are processed 250% faster than standard shipping

![Plot to visualize express vs standard processing](viz/processingtime.png)

## Proposed Measures

The stakeholder asked us to evaluate two scenarios: Handle all orders as express or have trucks on every day.

Trucks on every day would reduce the pickup time by 0.5 days, since orders that are ready on day 1 would still wait till day 2 to be shipped. Since the average pickup time is 1.5 days, the lead time wouldn't be substantially better.

Handling all orders as express would decrease lead time by ~36% and have the processing conforming to the stakeholder's initial expectations

![Boxplot to visualize express lead time](viz/boxplotexpress.png)

Lastly, the client should renegotiate with the logistics provider to either pay less, or get the contractually agreed 3 days to further decrease the lead time by 1.5 days, resulting in a final 5.5 days from taking the order to it being delivered at the customer's doorstep. This would be another improvement of ~21%.


---
For a more in-depth analysis and all technical details, check out the jupyter notebook [muesli_eda](https://github.com/GHLukasLang/muesli_lead_time/blob/main/muesli_eda.ipynb)!

