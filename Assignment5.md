Done

Here is a link to the SQL dataset: https://lite.datasette.io/?csv=https://raw.githubusercontent.com/fivethirtyeight/data/refs/heads/master/murder_2016/murder_2015_final.csv&csv=https://raw.githubusercontent.com/fivethirtyeight/data/refs/heads/master/murder_2016/murder_2016_prelim.csv#/data.csv?sql=select+murder_2015_final.city%2C+murder_2015_final.state%2C+murder_2015_final.%222014_murders%22%2C+murder_2015_final.%222015_murders%22%2C+murder_2016_prelim.%222016_murders%22%0Afrom+murder_2015_final%0Ajoin+murder_2016_prelim%0Aon+murder_2015_final.city+%3D+murder_2016_prelim.city%0Aorder+by+%222016_murders%22+desc&_size=max

Here is my final SQL query that made the dataset: 
select murder_2015_final.city, murder_2015_final.state, murder_2015_final."2014_murders", murder_2016_prelim."2015_murders", murder_2016_prelim."2016_murders"
from murder_2015_final
join murder_2016_prelim
on murder_2015_final.city = murder_2016_prelim.city
order by "2016_murders" desc

I decided to use the 2015 data from the 2015 dataset instead of the 2016 dataset because I compared the data from each dataset to the Brennan Center for Justice data on murder statistics in 2015. The 2015 dataset had numbers much closer to what the Brennan Center had. The 2016 dataset numbers on 2015 numbers were less than what the Brennan Center reported. Here is a link to the Brennan Center for Justice: https://www.brennancenter.org/sites/default/files/publications/Crime_Data_Dec2015.pdf 
