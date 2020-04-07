# BATTLE OF NEIGHBORHOOD

## Introduction

For some, customers, visiting shopping centers is an extraordinary method to unwind and live
it up during ends of the week and occasions. They can do shopping for food, feast at cafés,
shop at the different design outlets, watch motion pictures and perform a lot more exercises.
Shopping centers resemble a one-stop goal for a wide range of customers. For retailers, the focal area and the
huge group at the shopping centers gives an incredible appropriation channel to showcase
their items and administrations. Property designers are additionally exploiting this pattern to
construct all the more shopping centers to take into account the interest. Thus, there are
many shopping centers in the city of Kuala Lumpur and a lot more are being fabricated.
Opening shopping centers permits property engineers to procure predictable rental pay.
Obviously, similarly as with any business choice, opening another shopping center requires
genuine thought and is much surprisingly entangled. Especially, the area of the shopping
center is one of the most significant choices that will decide if the shopping center will be a
triumph or a disappointment.

## Business Problem
The goal of this capstone venture is to break down and choose the best areas in the Cairo,
Egypt to open shopping center. Utilizing information science philosophy and AI methods
like grouping, this venture intends to give answers for answer the business question: In
Cairo, Egypt if a property designer is hoping to open another shopping center, where might
you prescribe that they open it?

## Data
To solve the problem, we will need the following data:
• List of neighborhoods in Cairo. This characterizes the extent of this venture
which is bound to the city of cairo, the capital city of the nation of Egypt .
• Latitude and longitude directions of those areas. This is required so as to plot
the guide and furthermore to get the setting information.
• Venue information, especially information identified with shopping centers.
We will utilize this information to perform bunching on the areas.


## Wellsprings of information and strategies to separate them
The Wikipedia page contains a rundown of neighborhoods in Kuala Lumpur, with a sum of 70
neighborhoods. We will utilize web scratching systems to separate the information from the
Wikipedia page, with the assistance of Python requests and beautifulsoup packages. At that
point we will get the land directions of the areas utilizing Python Geocoder bundle which will
give us the scope and longitude directions of the areas.
From that point forward, we will utilize Foursquare API to get the venue data for those areas.
Foursquare has one of the biggest database of 105+ million places and is utilized by more than 125,000
engineers.
Foursquare API will give numerous categories of venue data, we are especially keen on the Shopping
Mall classification so as to assist us with solving the business issue set forward. This is a task that will
utilize numerous data science skills, from web scraping (Wikipedia), working with API (Foursquare),
data cleaning, data wrangling, to machine learning (K-means clustering) and map visualization (Folium).
In the following segment, we will introduce the Methodology segment where we will talk about the
means taken right now, the data analysis that we did and the machine learning technique that was
utilized.

## Methodology
Right off the bat, we have to get the rundown of neighborhoods in Cairo. Luckily, the
rundown is accessible in the Wikipedia page
We will do web scraping utilizing Python requests and beautifulsoup packages to remove the rundown of
neighborhoods information. Notwithstanding, this is only a rundown of names. We
have to get the geological facilitates as latitude and longitude so as to have the
option to utilize Foursquare API. To do as such, we will utilize the awesome
Geocoder package that will permit us to change over location into topographical
facilitates as scope and longitude. In the wake of social occasion the information, we
will populate the information into a pandas DataFrame and afterward visualize the
neighbourhoods in a guide utilizing Folium package. This permits us to play out a
once-over to make sure everything seems ok to ensure that the topographical
directions information returned by Geocoder are effectively plotted in Cairo city.
Next, we will utilize Foursquare API to get the best venues that are inside a range of
2000 meters. We have to enroll a Foursquare Developer Account so as to get the
Foursquare ID and Foursquare secret key. We at that point make API calls to
Foursquare going in the geological directions of the areas in a Python loop.
Foursquare will restore the venue data in JSON format and we will separate the
venue name, venue category, venue latitude and longitude. With the data, we can
check what number of venues were returned for every area and look at what
number of special classifications can be curated from all the brought venues back. At
that point, we will break down every area by gathering the lines by neighborhood
and taking the mean of the recurrence of event of every venue category. Thusly, we
are additionally setting up the data for use in bunching. Since we are breaking down
the "Shopping Mall" data, we will filter the "Shopping Mall" as venue classification
for the areas.
In conclusion, we will perform clustering on the information by utilizing k-means
clustering. K-means clustering calculation recognizes k number of centroids, and
afterward apportions each datum point to the closest bunch, while keeping the
centroids as little as could reasonably be expected. It is one of the least complex and
well known solo AI calculations and is especially fit to take care of the issue for this 
undertaking. We will group the areas into 3 clusters dependent on their recurrence of
event for "Shopping Mall". The outcomes will permit us to distinguish which
neighborhoods have higher centralization of shopping centers while which
neighborhoods have less number of shopping centers. In view of the event of shopping
centers in various neighborhoods, it will assist us with answering the inquiry about
which neighborhoods are generally appropriate to open new shopping centers

