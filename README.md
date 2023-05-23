# data_with_danny_8_weeks_sql_challenge

![Pizza](https://github.com/Aravindreddy-k/data_with_danny_8_weeks_sql_challenge/assets/113081704/d678a9b2-4b8b-4704-9029-d21432ec8b89)


Table 1: runners<br>
The runners table shows the registration_date for each new runner<br>

runner_id	registration_date <br>
1	2021-01-01<br>
2	2021-01-03<br>
3	2021-01-08<br>
4	2021-01-15<br>
Table 2: customer_orders<br>
Customer pizza orders are captured in the customer_orders table with 1 row for each individual pizza that is part of the order.<br>

The pizza_id relates to the type of pizza which was ordered whilst the exclusions are the ingredient_id values which should be removed from the pizza and the extras are the ingredient_id values which need to be added to the pizza.<br>

Note that customers can order multiple pizzas in a single order with varying exclusions and extras values even if the pizza is the same type!<br>

The exclusions and extras columns will need to be cleaned up before using them in your queries.<br>

order_id	customer_id	pizza_id	exclusions	extras	order_time<br>
1	101	1	 	 	2021-01-01 18:05:02<br>
2	101	1	 	 	2021-01-01 19:00:52<br>
3	102	1	 	 	2021-01-02 23:51:23<br>
3	102	2	 	NaN	2021-01-02 23:51:23<br>
4	103	1	4	 	2021-01-04 13:23:46<br>
4	103	1	4	 	2021-01-04 13:23:46<br>
4	103	2	4	 	2021-01-04 13:23:46<br>
5	104	1	null	1	2021-01-08 21:00:29<br>
6	101	2	null	null	2021-01-08 21:03:13<br>
7	105	2	null	1	2021-01-08 21:20:29<br>
8	102	1	null	null	2021-01-09 23:54:33<br>
9	103	1	4	1, 5	2021-01-10 11:22:59<br>
10	104	1	null	null	2021-01-11 18:34:49<br>
10	104	1	2, 6	1, 4	2021-01-11 18:34:49<br>
Table 3: runner_orders<br>
After each orders are received through the system - they are assigned to a runner - however not all orders are fully completed and can be cancelled by the restaurant or the customer.<br>

The pickup_time is the timestamp at which the runner arrives at the Pizza Runner headquarters to pick up the freshly cooked pizzas. The distance and duration fields are related to how far and long the runner had to travel to deliver the order to the respective customer.<br>

There are some known data issues with this table so be careful when using this in your queries - make sure to check the data types for each column in the schema SQL!<br>

order_id	runner_id	pickup_time	distance	duration	cancellation<br>
1	1	2021-01-01 18:15:34	20km	32 minutes	 <br>
2	1	2021-01-01 19:10:54	20km	27 minutes	 <br><br>
3	1	2021-01-03 00:12:37	13.4km	20 mins	NaN<br><br>
4	2	2021-01-04 13:53:03	23.4	40	NaN<br><br>
5	3	2021-01-08 21:10:57	10	15	NaN<br>
6	3	null	null	null	Restaurant Cancellation<br>
7	2	2020-01-08 21:30:45	25km	25mins	null<br>
8	2	2020-01-10 00:15:02	23.4 km	15 minute	null<br>
9	2	null	null	null	Customer Cancellation<br>
10	1	2020-01-11 18:50:20	10km	10minutes	null<br>
Table 4: pizza_names<br>
At the moment - Pizza Runner only has 2 pizzas available the Meat Lovers or Vegetarian!<br>

pizza_id	pizza_name<br>
1	Meat Lovers<br>
2	Vegetarian<br>
Table 5: pizza_recipes<br>
Each pizza_id has a standard set of toppings which are used as part of the pizza recipe.<br>

pizza_id	toppings<br>
1	1, 2, 3, 4, 5, 6, 8, 10<br>
2	4, 6, 7, 9, 11, 12<br>
Table 6: pizza_toppings<br>
This table contains all of the topping_name values with their corresponding topping_id value<br>

topping_id	topping_name<br>
1	Bacon<br>
2	BBQ Sauce<br>
3	Beef<br>
4	Cheese<br>
5	Chicken<br>
6	Mushrooms<br>
7	Onions<br>
8	Pepperoni<br>
9	Peppers<br>
10	Salami<br>
11	Tomatoes<br>
12	Tomato Sauce<br>
