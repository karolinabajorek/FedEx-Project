# FedEx Lane Optimization  - Project Overview
## The goal of this project is to investigate the capacity of Europe-Americas lane at Fedex in order to surface recommendations on efficient lane-level volume allocation acrocss services provided in the future.
Founded in 1971, FedEx is a global transportation and logistics company serving millions of customers across more than 220 countries and territories. The company provides four different international shipping services: International Economy and International Priority for parcels below 68kg, and International Economy Freight and International Priority Freight for shipments above 68kg.

The company encountered problems with volume volatility - there are days when they are short on capacity on Transatlantic lane (between Europe Region and Americas Region), predominantly for shipments going from Europe into the Americas. This puts at risk priority services since the transit time does not allow any flexibility to take next day flight (unlike economy services). Three customers (A, B, C) have been identified as large shipppers for Europe-Americas lane, and FedEx is strategizing volume allocation for the lane. The company would like to build more understanding on the volume allocation for Europe-Americas lane and learn how to increase network efficiency by maximizing flight utilisation. The shipments should be allocated to drive 2 primary objectives: 1) increase operational efficiency, and 2) drive predictability in periodic volumes shipped.
## Dataset Structure
The dataset consisted of 2 tables, including information about customers, shipments and their origins and destinations, as well as geographical regions and country descriptions.

<img width="624" alt="Screenshot 2025-01-29 at 19 30 26" src="https://github.com/user-attachments/assets/37a871f5-2bbd-4204-bde0-020d8c9e88eb" />

## Insights Summary
#### In order to evaluate lane performance, I focused on the following key metrics:
* **Yield:** The USD revenue per 1kg of charged weight.  
* **Charged-to-Actual Weight Ratio:** The ratio shows how much weight was charged per 1 kg of actual weight.  
* **Interquartile Range:** The difference between the 3rd and 1st quartiles of weekly weight charged measures the data's dispersion.  
* **% Dependence on Priority Services:** The percentage of weight charged shipped via FedEx priority services.  
#### Yield:
* Across customers, Customer C brought the most revenue per 1kg of weight charged on Europe-Americas shipments (4.86 USD/kg) while shipping the smallest volume on the route among  all customers (332,134 kg).  
* Customer C brought the highest yield on International Priority Freight (5.38 USD/kg) and International Priority Parcel shipping (3.43 USD/kg) for the Europe-Americas lane.  
* Considering Europe-Americas lane 1) for Customer A: economy parcel shipping is 3x pricier than priority service, and freight services are the same price. 2) For Customer B: economy freight shipping is 2.5x pricier than priority service, and parcel priority is cheaper than economy. 3) For Customer C: freight services are almost identically priced.  
#### Charged-to-Actual Weight Ratio:
* Across customers, Customer A had by far the highest overall charged-to-actual weight ratio(1.66) on Europe-Americas shipments.
* Customer A’s trend is consistent - having the highest charged-to-actual weight ratio across 17 of 18 analyzed weeks.
#### Interquartile Range:
* Across customers, Customer B had the highest Interquartile Range for weight charged on Europe-Americas shipments (19 142 kg).
* Within the distribution of average shipment size, Customer B also displays the highest dispersion of values (IQR 354 kg).
#### % Dependence on Priority Services:
* All the customers present staggering dependence on priority services for their Europe-Americas shipments - Customer A was almost entirely dependent on priority (99.41%).
* Customer A is highly dependent on priority services for its Europe-Americas shipments. However, it is least dependent on the Europe-Americas lane of all the customers (56.02%).
## Recommendations:
* **Prioritize priority shipments for Customer C** in the Europe-Americas lane during peak times. These have the highest yield on priority shipments among customers, for parcel and freight shipments, and the lowest volatility in weekly weight charged.
* **Fix evident pricing errors for all Customers A, B, and C**, where priority pricing is cheaper than the economy or of equal price as the economy, which encourages choosing priority over economy services.
* **Incentivize dimensional weight reduction for Customer A:** 1) Introduce tiered discounts for shipments that meet specific dimensional weight efficiency thresholds. 2) Offer incentives for better packaging practices, such as rebates for shipments where the actual weight is closer to the charged weight.
* **Introduce a contractual agreement to ensure consistent weekly volumes or caps on weekly volumes** on Europe-Americas priority shipments, especially for highly volatile and voluminous Customer B and, inconsistent Customer A, reducing strain during peak times.
* **Negotiate a flexible shipping agreement** - where Customers B and A allow shifting some priority shipments to next-day flights during peak times.  
* **Promote and offer price incentives on alternate lanes where feasible for economy shipments to encourage redistribution of shipments.** This could free up capacity for priority products in the Europe-Americas lane.

## Dashboard
The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/karolina.bajorek/viz/FedexAnalysisFinal/Dashboard1). This dashboard enables users to filter by customer, linehaul type, linehaul, service type and priority and focuses on trends and values on customer, service and lane levels.
![Dashboard 1](https://github.com/user-attachments/assets/602534e6-3433-4e4d-9c26-aae45bdf81ac)
## Presentation Sample
The presentation created for the commercial execution team walks through the insights and recommendations above and can be found [here]([url](https://github.com/karolinabajorek/FedEx-Project/blob/main/FedEx%20Project.pdf)). Some extracts are presented below for easy viewing.

<img width="1156" alt="Screenshot 2025-01-30 at 14 37 02" src="https://github.com/user-attachments/assets/00dd5ab3-5b22-4e00-8efe-86d188958ff4" />
<img width="1183" alt="Screenshot 2025-01-30 at 14 37 18" src="https://github.com/user-attachments/assets/9d413e04-0fa3-4047-8991-e01cd2f65473" />
<img width="1191" alt="Screenshot 2025-01-30 at 14 37 30" src="https://github.com/user-attachments/assets/a58d5439-5ba3-4d4a-a030-e1c9a8f12eff" />

