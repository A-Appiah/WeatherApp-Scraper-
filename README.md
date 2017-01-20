# WeatherApp-Scraper-
This is the back end code for the Weather App, which uses PHP and FTP and Ajax to give you the weather in a 3 day forecast. 

<?php

$city=$_GET['city'];

$city=str_replace(" ", "", $city);

$contents=file_get_contents("http://http://www.weather-forecast.com/locations/Milpitas/forecasts/latest");

preg_match( ' /3 Day WEather Forecast:<\/b><span class="phrase">(/*?)</s', $contents, $matches);

echo $matches[1];



?>
