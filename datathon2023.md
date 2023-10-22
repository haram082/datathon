Datathon 2023: Investigating Airline Delays During College Student
Travel in the 5Cs
================
2023-10-21

## By Haram Yoon and Kartika Santonso

College students often experience the frustration of delayed flights
when traveling home for academic breaks. As students book tickets home
for the holidays, they want to choose airlines that are less likely to
experience delays departing from major college town airports.

In this report, we analyzed airline flight data to uncover insights into
delay rates for different carriers around college student travel
periods. They focused on flights leaving college town airports during
the typical breaks within the academic calendar.

The goal was to identify airlines that tend to have higher versus lower
delays when serving college student travelers. The findings can help
students make informed decisions when booking flights home for
Thanksgiving, winter break, spring break, and other peak travel times.

We loaded historical flight data into R and filtered for flights
departing from the major airports, Ontario and LAX, near the 5cs. We
calculated delay rates for different airlines during the busy student
travel periods. Finally, we visualized the airline delay patterns to
highlight carriers with relatively high and low delays.

The report outlines the analysis process and key findings. The results
provide data-driven guidance to help college students choose airlines
with the best on-time reliability when planning trips home.

### Delay Rates for Major Carriers During Holiday Travel Out of LAX and Ontario

First, I filter the flights dataset to only include those originating
from LAX or Ontario airports. I then create a date variable from the
month and day columns. Next, I isolated flights during the busy holiday
travel periods in October, November, December 2023 and March 2024. I
then group the data by carrier and the specified date ranges. For each
group, I calculate the proportion of flights delayed Finally, I
visualize the delay rate for each carrier and time period in a stacked
bar chart.
![](datathon2023_files/figure-gfm/unnamed-chunk-2-1.png)<!-- --> This
chart shows the relative delay rates for major carriers during the
specified holiday travel periods out of LAX and Ontario. We can see that
some carriers experienced higher delays than others during the busy
travel times. This information could help college student choose the
best airline for holidays from the 5Cs. For example, Frontier Airlines
have a big proportion of the delays found before winter break. Companies
such as United consistently stay on the lower proportions of delays
regardless of seasons. Our plot will help 5c students to figure out
which airlines are more likely to have delays per break.

### Exploring Airline Delay Patterns for Student Travel

To dig deeper into airline delays during student travel periods, I
calculated the average delay time for flights departing college towns
during academic breaks.

First, I filtered the data to only include flights leaving LAX or
Ontario airports, and limited to the break travel periods previously
identified. I then grouped the flights by origin city, destination, and
airline carrier. For each group, I calculated the total delay, number of
flights, and mean delay time. Finally, I visualized the mean delay time
for each airline and destination as a faceted dot plot w margins of
errors.

![](datathon2023_files/figure-gfm/unnamed-chunk-4-1.png)<!-- --> This
visualization highlights the carriers and destinations with the lowest
and highest average delays during student travel periods. Students can
use this to make more informed airline selections when booking flights
home from college. This is help college students figure out which
airline to take from either the Ontario and LAX. It even tells us which
airlines are historically available at these airports and their mean
delay times. For example, if you go to Chicago from LAX, Alaska Airlines
should not be your first option.

### Mapping Delays in Arriving Flights to LAX and ONT

![](datathon2023_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

Next, we took a subset of the dataset containing only flights arriving
at LAX or ONT, and visualized these flights.

This interactive map visualizes all flights arriving at LAX and ONT from
every other airport in the US. Each airport is colored based on the mean
delay that flights to LAX and ONT experience. If you click on the
points, you will be able to see the airport name, the number of flights
to LAX and ONT, and the mean delay for these flights.

This allows Claremont College students to see which flight routes may
experience delays, which would allow them to better select flights to
take when returning home over breaks.

### Ethics

We acknowledge that in generalizing flight delays for airlines and
routes, this could result in a loss of sales for these airlines and
paths, which could ultimately impact workers for these airlines. We also
realize that since we are using past data, it isn’t indictative of
future and present conditions for these airlines and routes.

## Github Link

<https://github.com/haram082/datathon.git>
