# WebApp-MBTA
 Team members: Linhao Jiang, Jasmine Zhang

# Project Overview

Our project aimed to assist users in locating the nearest MBTA station to their input address and checking its wheelchair accessibility status as well as other information like nearby restaurants and events. We use MAPBOX API to convert user-input addresses into coordinates, and then MBTA API with these coordinates to find the nearest subway station and assess its wheelchair accessibility status. Other APIs like OpenWeather for weather forecasts, Ticketmaster for local events, and Google Maps for restaurant recommendations. 

The core functionality of our application stays in the mbta_helper.py page, which interacts with those external APIs. The Flask framework is powered by app.py, it sets up the website and routing. When the user lands on the first page, will see a simple form where the user inputs their address via index.html, and receives detailed information on results.html, with error handling implemented in error.html. Our project functions beyond merely finding the nearest MBTA station, we also aim to include valuable local context and real-time updates. 


# Reflection

One thing we changed very late in the process is that we decided to use the Google Map API to get the weather information and the city name because we found if we use MBTA API, for these places without a station nearby, we cannot output weather data, which is not logical. For the nearby restaurants for stations, we planned to use Yelp API but we found it very hard to apply and not intuitive to use, so we pivoted to Google Map API. ![Yelp API Challenge](images/Yelp_API_Challenge.png)


For mbta_helper.py, our initial version was stored in help_attempt.py, later we decided to use the template that Professor Li provided because it was more consistent with using urllib.request, in contrast, we initially mixed 'urllib.request' and 'request'. We believe that having consistency in using libraries can make code more uniform and easier to read.

For team collaboration, we initially planned frequent in-person meetings but due to scheduling conflicts, the approach was adjusted. Jasmine took the lead on initial development, laying down the groundwork for the application, Linhao served as the debugger and perfectionist, fixed Jasmine's bugs, and enhanced functionality by applying additional APIs. Despite the shift from our initial plans, our team dynamic is very good, we had active communication through online discussions, and we also used live-share, to effectively address overlap in progress. 

Ai helped us on the project with HTML template styling.
![html_formatting](images/html_formatting.png)
as well as understanding Google Map API data structure:
![google_map_api](images/google_map_api.png)


Overall, AI serves as an assistant, who can offer guidance and support in areas where we lack expertise and knowledge. 