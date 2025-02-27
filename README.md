
# Investigating the Cost of Living Crisis, Climate and its Effect on the NHS

I was assigned this project by a junior doctor in midst of talks about their wages with the government hopelessly ending in frustration nearly everytime. I was tasked with investigating how many different factors which contribute to the cost of living for a person impacts the NHS.

I started out with acquiring data about the **total attendances** and **total emergency** attendences across all NHS hospitals in the UK by going to the NHS website. Here is an illustration of the dataset:

![SS2](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.14.34.png)

I then acquired another dataset that took into account **55** different aspects that contributes to the cost of living. The following features were involved in this dataset:

-----

**x1	Meal, Inexpensive Restaurant (USD)**

**x2	Meal for 2 People, Mid-range Restaurant, Three-course (USD)**

**x3	McMeal at McDonalds (or Equivalent Combo Meal) (USD)**

**x4	Domestic Beer (0.5 liter draught, in restaurants) (USD)**

**x5	Imported Beer (0.33 liter bottle, in restaurants) (USD)**

**x6	Cappuccino (regular, in restaurants) (USD)**

**x7	Coke/Pepsi (0.33 liter bottle, in restaurants) (USD)**

**x8	Water (0.33 liter bottle, in restaurants) (USD)**

**x9	Milk (regular), (1 liter) (USD)**

**x10	Loaf of Fresh White Bread (500g) (USD)**

**x11	Rice (white), (1kg) (USD)**

**x12	Eggs (regular) (12) (USD)**

**x13	Local Cheese (1kg) (USD)**

**x14	Chicken Fillets (1kg) (USD)**

**x15	Beef Round (1kg) (or Equivalent Back Leg Red Meat) (USD)**

**x16	Apples (1kg) (USD)**

**x17	Banana (1kg) (USD)**

**x18	Oranges (1kg) (USD)**

**x19	Tomato (1kg) (USD)**

**x20	Potato (1kg) (USD)**

**x21	Onion (1kg) (USD)**

**x22	Lettuce (1 head) (USD)**

**x23	Water (1.5 liter bottle, at the market) (USD)**

**x24	Bottle of Wine (Mid-Range, at the market) (USD)**

**x25	Domestic Beer (0.5 liter bottle, at the market) (USD)**

**x26	Imported Beer (0.33 liter bottle, at the market) (USD)**

**x27	Cigarettes 20 Pack (Marlboro) (USD)**

**x28	One-way Ticket (Local Transport) (USD)**

**x29	Monthly Pass (Regular Price) (USD)**

**x30	Taxi Start (Normal Tariff) (USD)**

**x31	Taxi 1km (Normal Tariff) (USD)**

**x32	Taxi 1hour Waiting (Normal Tariff) (USD)**

**x33	Gasoline (1 liter) (USD)**

**x34	Volkswagen Golf 1.4 90 KW Trendline (Or Equivalent New Car) (USD)**

**x35	Toyota Corolla Sedan 1.6l 97kW Comfort (Or Equivalent New Car) (USD)**

**x36	Basic (Electricity, Heating, Cooling, Water, Garbage) for 85m2 Apartment (USD)**

**x37	1 min. of Prepaid Mobile Tariff Local (No Discounts or Plans) (USD)**

**x38	Internet (60 Mbps or More, Unlimited Data, Cable/ADSL) (USD)**

**x39	Fitness Club, Monthly Fee for 1 Adult (USD)**

**x40	Tennis Court Rent (1 Hour on Weekend) (USD)**

**x41	Cinema, International Release, 1 Seat (USD)**

**x42	Preschool (or Kindergarten), Full Day, Private, Monthly for 1 Child (USD)**

**x43	International Primary School, Yearly for 1 Child (USD)**

**x44	1 Pair of Jeans (Levis 501 Or Similar) (USD)**

**x45	1 Summer Dress in a Chain Store (Zara, H&M, …) (USD)**

**x46	1 Pair of Nike Running Shoes (Mid-Range) (USD)**

**x47	1 Pair of Men Leather Business Shoes (USD)**

**x48	Apartment (1 bedroom) in City Centre (USD)**

**x49	Apartment (1 bedroom) Outside of Centre (USD)**

**x50	Apartment (3 bedrooms) in City Centre (USD)**

**x51	Apartment (3 bedrooms) Outside of Centre (USD)**

**x52	Price per Square Meter to Buy Apartment in City Centre (USD)**

**x53	Price per Square Meter to Buy Apartment Outside of Centre (USD)**

**x54	Average Monthly Net Salary (After Tax) (USD)**

**x55	Mortgage Interest Rate in Percentages (%), Yearly, for 20 Years Fixed-Rate**

-----

Here is an illustration of the cost of living dataset:

![SS1](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.15.34.png)

Finally, due to a growing suspicion amongst junior doctors that changes in weather conditions, especially rain, causes an increase in visits to the hospital, I set out to acquire a publically available dataset from the MET office and averaged their data from many different cities in the UK provided by 5 of their weather stations.

Here is an illustration of the MET Office weather office dataset:

![SS3](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.13.28.png)

I then merged the three datasets by using various functionalities in Excel such as XLOOKUPs and AVERAGEIFs to merge the NHS, weather and cost of living datasets together.

Here is an illustration of the fully merged dataset:

![SS4](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.16.01.png)

After finishing preprocessing and cleaning all these datasets I set out to first get a bird's eye view across all the variables in my dataset and to essentially quickly eyeball relationships between different features by plotting out a heatmap of correlations between average normal and emergency attendances to variables in the cost of living dataset and the weather dataset.

![SS5](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.12.27.png)

Here we can see that the weather variables makes no difference to the amount of visits and attendances made to the hospital. All have extremely small and insignificant correlations as shown by the last 5 rows of the heatmap. Therefore, this growing suspicion amongst the junior doctors is simply false.


-----

We can also see a significant (compared to other variables in this heatmap) positive correlation between x3 and average hospital attendances and average emergency hospital attendances of 0.40 and 0.46 respectively. Normally, this relationship would mean that the greater the expenditure on fast food restaurant chains, the greater the impact on the NHS as fast food is notoriously unhealthy. 

![SS6](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.07.56.png)

![SS7](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.08.28.png)

This relationship could also mean that places with higher meal prices and expenditure will tend to be indicative of more urbanised cities where healthcare structure will be more developed, e.g. London.

Cities where McDonald's meals are more expensive may have a higher overall cost of living. These cities might also have better healthcare facilities and access, leading to higher healthcare attendance rates.

In economically prosperous areas, residents may have higher incomes, allowing them to afford both higher-priced meals and better healthcare services.


-----

Addtionally, we can also see another relationship which consists of a negative correlation between the attendances in the hospital and x52 and x53.

![SS8](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.08.39.png)

![SS9](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.42.12.png)

This could be described due to the following reasons: 

Higher property prices, both in city centers and outside, often reflect a wealthier population or higher economic status. In affluent areas, individuals might have better access to private healthcare services, reducing reliance on emergency services provided by public health systems. People with higher incomes might also be more proactive about health care, leading to fewer emergency admissions.

The negative correlation could indicate that as housing prices rise, the residents might be able to afford more comprehensive health insurance or private healthcare options, which reduces their dependence on emergency services

Urban centers with high property prices might invest more in public health initiatives and infrastructure. Better urban planning can reduce the need for emergency services by improving overall health and safety conditions.

-----

There is also a negative correlation between the price for daycare for 1 child and the amount of emergency attendances in the NHS. 

![SS10](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.43.25.png)

An increase in the price of full-day, private preschool for one child could potentially decrease emergency NHS admissions for several reasons:

--> Higher costs might lead to selective enrollment where only families with sufficient financial resources can afford private preschool. These families may also have better access to healthcare, preventative measures, and healthier lifestyles, leading to fewer emergency admissions.

--> Higher costs may reduce the overall number of children enrolled in full-day private preschools. Consequently, children might stay home where they are less exposed to infectious diseases and injuries that can occur in group settings, thereby potentially reducing emergency admissions.

--> When parents cannot afford private preschool, they might opt to stay home or adjust their work schedules to take care of their children. Increased parental involvement can lead to better monitoring of children’s health and quicker responses to minor illnesses or injuries before they escalate to emergencies.

--> Families that can afford higher preschool fees might also have better access to regular and preventative healthcare for their children. This can result in early detection and treatment of health issues, reducing the need for emergency care.

--> Higher preschool costs can indicate better overall socioeconomic conditions for families who can afford it. Higher socioeconomic status is often associated with better health outcomes and lower emergency healthcare needs due to factors like better nutrition, safer living environments, and comprehensive health insurance coverage.

--> Families paying higher preschool fees might prioritize health and safety standards more rigorously, choosing facilities with better healthcare policies, safer environments, and lower student-to-teacher ratios, reducing the likelihood of accidents or health issues that necessitate emergency care.

--> A focus on higher-cost preschools might lead to more resources being allocated towards quality early childhood education, including health and safety measures, thereby reducing the risk of emergencies.

-----

Another unexpected insight would a moderate positive correlation between cappucino prices and hospital attendances - with the correlations of 0.23 and 0.22 respectively. 

![SS12](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2023.00.52.png)

![SS11](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2023.00.46.png)


This relationship can be explained due to the following reasons: 

--> Higher cappuccino prices are typically found in more affluent neighborhoods. These areas often have vibrant social scenes with frequent social interactions, meetings, and gatherings in cafes.

--> Residents of these affluent areas tend to spend more time in social settings like cafes. This increased social engagement can lead to a more active social lifestyle, which, while generally positive, can also contribute to increased stress levels due to busier schedules and social pressures.

--> The heightened social activity and associated stress might lead to more minor health issues, prompting more visits to emergency services. For example, stress-related conditions like anxiety or minor accidents during social events could lead to emergency room visits.

--> Thus, the price of cappuccino can act as a proxy for the level of social activity and interaction in an area. Higher cappuccino prices, indicating a socially active and affluent area, correlate with higher emergency admissions due to the lifestyle-related health impacts of these social behaviors.

-----

Furthermore, we can see that when we sum all the aspects that may contribute to the cost of living of one person, there is a mild correlation after we remove a few outliers and then standardise values to make sure that every feature has an equal say in the results.

![SS13](https://github.com/VishRMehta/Cost-of-Living-Climate-and-the-NHS/blob/main/nhs-images/Screenshot%202024-08-06%20at%2022.16.44.png)

The result is a mild negative correlation, which is a finding that supports many numerous articles about how cost of living negatively impacts the NHS but based on the plot we perhaps may need to work harder and delve deeper to uncover a slightly stronger relationship as our R2 score is relatively low which is suprising given the sheer amalagamation of factors we have undertaken.

