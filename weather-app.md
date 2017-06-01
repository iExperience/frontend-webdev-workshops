Responsive, web-based weather app

Because I'm tired of sifting through hundreds of ads to find out what I need to wear today

Requirements

You are tasked with building a single-page, responsive weather application. Here are some loose requirements to get you started:

You should use forecast.io's API to get your data

The API needs a latitude and longitude. Here is how you should get them:

Read more about how to use the Geolocation API of browsers.
Based on this reading, determine if the user allows you to get their estimated location.
If the API is not available in the browser, or if the user denies your request, or if it's been more than a few seconds since you asked, use the IP API to detect the user's location.
Using Google's Reverse Geocoding API, find out the closest city to the latitude/longitude pair you obtained from either #2 or #3 above.

This city name will be displayed in the interface, and below it, the latitude/longitude pair will be used to query forecast.io's API and display a panel that looks like the following:

weather panel

One of your tasks will be to figure out how this interface will adapt to different devices. A nice way to do it would be to have a swipe action happening on mobiles, to move from day to day. Experiment and find what works best :)
Use a nice open font, some open-source icons and try to make the interface look particularily nice. Perhaps a transition or two would help make the loading time less noticeable?
