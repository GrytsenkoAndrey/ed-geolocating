# ed-geolocating

On a project, we were using the Google Maps API to translate a US postal code into a latitude and longitude.

I bumped into a problem where a small number of postal codes would return a null result, despite being valid US postal codes.

I have no idea why this was the case. I thought maybe this postal code happened to overlap with a postal code in another country, so it just gave up and returned no results?

It didn't really matter why Google Maps was doing this for a handful of postal codes. I just wanted it to work.

So instead of sending just 12345 to the API, I would append the country code: 12345 US. This worked every time.
