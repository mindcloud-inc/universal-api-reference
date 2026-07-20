# <img src="https://images.mindcloud.co/apps/icons/openweather-icon_1776187550129.png" alt="OpenWeather logo" width="28" height="28"> OpenWeather: Universal API

OpenWeather provides weather, forecast, air pollution, geocoding, map, and related environmental data APIs for locations worldwide.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openWeather/latest
- **Actions:** 58
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openweathermap.org
- **Vendor API docs:** https://openweathermap.org/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Weather](actions/get-current-weather.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-current-weather?connectionId=$CONNECTION_ID&lat=1&lon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (58)

### Accumulated Precipitation

| Action | Method | Description |
| --- | --- | --- |
| [Get Accumulated Precipitation](actions/get-accumulated-precipitation.md) | GET | Retrieves accumulated precipitation data from OpenWeather. |

### Accumulated Temperature

| Action | Method | Description |
| --- | --- | --- |
| [Get Accumulated Temperature](actions/get-accumulated-temperature.md) | GET | Retrieves accumulated temperature data from OpenWeather. |

### Ai Weather Session

| Action | Method | Description |
| --- | --- | --- |
| [Resume AI Weather Session](actions/resume-ai-weather-session.md) | PUT | Continues an OpenWeather AI weather assistant session. |
| [Start AI Weather Session](actions/start-ai-weather-session.md) | POST | Starts an OpenWeather AI weather assistant session. |

### Air Pollution

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Air Pollution](actions/get-current-air-pollution.md) | GET | Retrieves current air pollution data from OpenWeather. |

### Air Pollution Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Air Pollution Forecast](actions/get-air-pollution-forecast.md) | GET | Retrieves an air pollution forecast from OpenWeather. |

### Air Pollution History

| Action | Method | Description |
| --- | --- | --- |
| [Get Air Pollution History](actions/get-air-pollution-history.md) | GET | Retrieves air pollution history from OpenWeather. |

### Climatic Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Climatic Forecast](actions/get-climatic-forecast.md) | GET | Retrieves a 30-day climate forecast from OpenWeather by coordinates. |
| [Get Climatic Forecast by City ID](actions/get-climatic-forecast-by-city-id.md) | GET | Retrieves a 30-day climate forecast from OpenWeather by city ID. |
| [Get Climatic Forecast by City Name](actions/get-climatic-forecast-by-city-name.md) | GET | Retrieves a 30-day climate forecast from OpenWeather by city name. |
| [Get Climatic Forecast by ZIP](actions/get-climatic-forecast-by-zip.md) | GET | Retrieves a 30-day climate forecast from OpenWeather by ZIP code. |

### Current Weather

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Weather](actions/get-current-weather.md) | GET | Retrieves current weather from OpenWeather by coordinates. |
| [Get Current Weather by City ID](actions/get-current-weather-by-city-id.md) | GET | Retrieves current weather from OpenWeather by city ID. |
| [Get Current Weather by City Name](actions/get-current-weather-by-city-name.md) | GET | Retrieves current weather from OpenWeather by city name. |
| [Get Current Weather by ZIP](actions/get-current-weather-by-zip.md) | GET | Retrieves current weather from OpenWeather by ZIP code. |

### Daily Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Forecast](actions/get-daily-forecast.md) | GET | Retrieves a daily forecast from OpenWeather by coordinates. |
| [Get Daily Forecast by City ID](actions/get-daily-forecast-by-city-id.md) | GET | Retrieves a daily forecast from OpenWeather by city ID. |
| [Get Daily Forecast by City Name](actions/get-daily-forecast-by-city-name.md) | GET | Retrieves a daily forecast from OpenWeather by city name. |
| [Get Daily Forecast by ZIP](actions/get-daily-forecast-by-zip.md) | GET | Retrieves a daily forecast from OpenWeather by ZIP code. |

### Daily Weather Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get One Call Daily Summary](actions/get-one-call-daily-summary.md) | GET | Retrieves a One Call daily summary from OpenWeather. |

### Fire Weather Index

| Action | Method | Description |
| --- | --- | --- |
| [Get Fire Weather Index](actions/get-fire-weather-index.md) | GET | Retrieves the fire weather index from OpenWeather. |

### Fire Weather Index Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Fire Weather Index Forecast](actions/get-fire-weather-index-forecast.md) | GET | Retrieves a fire weather index forecast from OpenWeather. |

### Fire Weather Map Tile

| Action | Method | Description |
| --- | --- | --- |
| [Get Fire Weather Map Tile](actions/get-fire-weather-map-tile.md) | GET | Retrieves a fire weather map tile from OpenWeather. |

### Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get 5 Day Forecast](actions/get-five-day-forecast.md) | GET | Retrieves a 5-day forecast from OpenWeather by coordinates. |
| [Get 5 Day Forecast by City ID](actions/get-five-day-forecast-by-city-id.md) | GET | Retrieves a 5-day forecast from OpenWeather by city ID. |
| [Get 5 Day Forecast by City Name](actions/get-five-day-forecast-by-city-name.md) | GET | Retrieves a 5-day forecast from OpenWeather by city name. |
| [Get 5 Day Forecast by ZIP](actions/get-five-day-forecast-by-zip.md) | GET | Retrieves a 5-day forecast from OpenWeather by ZIP code. |

### Historical Weather

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Weather](actions/get-historical-weather.md) | GET | Retrieves historical weather data from OpenWeather. |

### Hourly Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Hourly Forecast](actions/get-hourly-forecast.md) | GET | Retrieves an hourly forecast from OpenWeather by coordinates. |
| [Get Hourly Forecast by City ID](actions/get-hourly-forecast-by-city-id.md) | GET | Retrieves an hourly forecast from OpenWeather by city ID. |
| [Get Hourly Forecast by City Name](actions/get-hourly-forecast-by-city-name.md) | GET | Retrieves an hourly forecast from OpenWeather by city name. |
| [Get Hourly Forecast by ZIP](actions/get-hourly-forecast-by-zip.md) | GET | Retrieves an hourly forecast from OpenWeather by ZIP code. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Geocode Location by Name](actions/geocode-location-by-name.md) | GET | Finds matching OpenWeather locations by name. |
| [Geocode ZIP Code](actions/geocode-zip-code.md) | GET | Finds an OpenWeather location by ZIP code. |
| [Reverse Geocode Coordinates](actions/reverse-geocode-coordinates.md) | GET | Finds OpenWeather locations by geographic coordinates. |

### One Call Time Machine

| Action | Method | Description |
| --- | --- | --- |
| [Get One Call Time Machine](actions/get-one-call-time-machine.md) | GET | Retrieves One Call weather from OpenWeather for a timestamp. |

### One Call Weather

| Action | Method | Description |
| --- | --- | --- |
| [Get One Call Weather](actions/get-one-call-weather.md) | GET | Retrieves One Call weather data from OpenWeather. |

### Solar Interval Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Solar Interval Data](actions/get-solar-interval-data.md) | GET | Retrieves solar interval data from OpenWeather. |

### Solar Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Solar Location](actions/create-solar-location.md) | POST | Creates a solar location in OpenWeather. |
| [Delete Solar Location](actions/delete-solar-location.md) | DELETE | Deletes a solar location from OpenWeather. |
| [Get Solar Location](actions/get-solar-location.md) | GET | Retrieves a solar location from OpenWeather. |
| [List Solar Locations](actions/list-solar-locations.md) | GET | Lists solar locations in OpenWeather. |

### Solar Panel

| Action | Method | Description |
| --- | --- | --- |
| [Create Solar Panel](actions/create-solar-panel.md) | POST | Creates a solar panel in OpenWeather. |
| [Delete Solar Panel](actions/delete-solar-panel.md) | DELETE | Deletes a solar panel from OpenWeather. |
| [Get Solar Panel](actions/get-solar-panel.md) | GET | Retrieves a solar panel from OpenWeather. |
| [List Solar Panels](actions/list-solar-panels.md) | GET | Lists solar panels in OpenWeather. |

### Statistical Weather

| Action | Method | Description |
| --- | --- | --- |
| [Get Statistical Weather by Day](actions/get-statistical-weather-by-day.md) | GET | Retrieves daily weather statistics from OpenWeather. |
| [Get Statistical Weather by Month](actions/get-statistical-weather-by-month.md) | GET | Retrieves monthly weather statistics from OpenWeather. |
| [Get Statistical Weather by Year](actions/get-statistical-weather-by-year.md) | GET | Retrieves yearly weather statistics from OpenWeather. |

### Weather Map Tile

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Map Tile](actions/get-weather-map-tile.md) | GET | Retrieves a weather map tile from OpenWeather. |

### Weather Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Overview](actions/get-weather-overview.md) | GET | Retrieves an OpenWeather AI weather overview by date. |

### Weather Station

| Action | Method | Description |
| --- | --- | --- |
| [Create Weather Station](actions/create-weather-station.md) | POST | Creates a weather station in your OpenWeather account. |
| [Delete Weather Station](actions/delete-weather-station.md) | DELETE | Deletes a weather station from your OpenWeather account. |
| [Get Weather Station](actions/get-weather-station.md) | GET | Retrieves a weather station from your OpenWeather account. |
| [List Weather Stations](actions/list-weather-stations.md) | GET | Lists weather stations in your OpenWeather account. |
| [Update Weather Station](actions/update-weather-station.md) | PUT | Updates a weather station in your OpenWeather account. |

### Weather Station Measurements

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregated Weather Station Measurements](actions/get-aggregated-weather-station-measurements.md) | GET | Retrieves aggregated weather station measurements from OpenWeather. |
| [Upload Weather Station Measurements](actions/upload-weather-station-measurements.md) | POST | Uploads weather station measurements to OpenWeather. |

