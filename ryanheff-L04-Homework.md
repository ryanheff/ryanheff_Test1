<h1>L04 Homework</h1><br>
Ryan Heffernan<br>
Instructor: Jim Byers<br>
7/18/2016<br>

1.Look at the head and the tail of chipotle.tsv in the data subdirectory of this repo. Think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

The columns can be explained as follows:

order_id: The order each items belongs to.
quantity: The number of each particular item purchased for each order.
item_name: The name of the item purchased.
choice_description: The options selected for each item.
item_price: The price of the item.c

Each row identifies a unique item per customer order. In other words, if I ordered 3 Steak Burritos and 4 Chicken Bowls, this would be represented by 2 rows, both with the same order_id. 


2.How many orders do there appear to be?

1834 (the command below counts the column title).

$ cut -f 1 chipotle.tsv | uniq | wc -l
1835


3.How many lines are in this file?

$ wc -l chipotle.tsv
4623 chipotle.tsv


4.Which burrito is more popular, steak or chicken?

$ grep "Chicken Burrito" chipotle.tsv | wc -l
553

$ grep "Steak Burrito" chipotle.tsv | wc -l
368


5.Do chicken burritos more often have black beans or pinto beans?

$ grep "Chicken Burrito" chipotle.tsv | grep "Pinto" | wc -l
105

$ grep "Chicken Burrito" chipotle.tsv | grep "Black" | wc -l
282


6.Make a list of all of the CSV or TSV files in the our class repo. repo (using a single command). You will be working on your local repo on your laptop. Think about how wildcard characters can help you with this task.

$ find . -name '*.*sv'<br>
./data/airlines.csv<br>
./data/Airline_on_time_west_coast.csv<br>
./data/bank-additional.csv<br>
./data/bikeshare.csv<br>
./data/chipotle.tsv<br>
./data/citibike_feb2014.csv<br>
./data/drinks.csv<br>
./data/drones.csv<br>
./data/hitters.csv<br>
./data/icecream.csv<br>
./data/imdb_1000.csv<br>
./data/mtcars.csv<br>
./data/NBA_players_2015.csv<br>
./data/ozone.csv<br>
./data/pronto_cycle_share/2015_station_data.csv<br>
./data/pronto_cycle_share/2015_trip_data.csv<br>
./data/pronto_cycle_share/2015_weather_data.csv<br>
./data/rossmann.csv<br>
./data/rt_critics.csv<br>
./data/sms.tsv<br>
./data/stores.csv<br>
./data/syria.csv<br>
./data/time_series_train.csv<br>
./data/titanic.csv<br>
./data/ufo.csv<br>
./data/vehicles_test.csv<br>
./data/vehicles_train.csv<br>
./data/yelp.csv<br>


7.Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files of our class repo.

$ grep -ri "Dictionary" | wc -l
100
