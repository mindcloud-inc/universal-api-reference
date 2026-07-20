# OpenWeather: Native API Reference

A consolidated summary of OpenWeather's API configuration and 58 documented operations, with links to official documentation.

- **Official docs:** https://openweathermap.org/api
- **API base URL:** `https://api.openweathermap.org`

## Authentication

### API Key

Authenticate with an OpenWeather API key sent as the shared `appid` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Your OpenWeather API key.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://openweathermap.org/faq#error401)

## Endpoints (58 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Solar Location](actions/create-solar-location.md) | `POST https://api.openweathermap.org/energy/2.0/locations` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Create Solar Panel](actions/create-solar-panel.md) | `POST https://api.openweathermap.org/energy/2.0/location/:locationId/panels` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Create Weather Station](actions/create-weather-station.md) | `POST /data/3.0/stations` | [docs](https://openweathermap.org/stations) |
| [Delete Solar Location](actions/delete-solar-location.md) | `DELETE https://api.openweathermap.org/energy/2.0/location/:locationId` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Delete Solar Panel](actions/delete-solar-panel.md) | `DELETE https://api.openweathermap.org/energy/2.0/panel/:panelId` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Delete Weather Station](actions/delete-weather-station.md) | `DELETE /data/3.0/stations/:stationId` | [docs](https://openweathermap.org/stations) |
| [Geocode Location by Name](actions/geocode-location-by-name.md) | `GET /geo/1.0/direct` | [docs](https://openweathermap.org/api/geocoding-api) |
| [Geocode ZIP Code](actions/geocode-zip-code.md) | `GET /geo/1.0/zip` | [docs](https://openweathermap.org/api/geocoding-api) |
| [Get Accumulated Precipitation](actions/get-accumulated-precipitation.md) | `GET https://history.openweathermap.org/data/2.5/history/accumulated_precipitation` | [docs](https://old.openweathermap.org/api/accumulated-parameters) |
| [Get Accumulated Temperature](actions/get-accumulated-temperature.md) | `GET https://history.openweathermap.org/data/2.5/history/accumulated_temperature` | [docs](https://old.openweathermap.org/api/accumulated-parameters) |
| [Get Aggregated Weather Station Measurements](actions/get-aggregated-weather-station-measurements.md) | `GET /data/3.0/measurements` | [docs](https://openweathermap.org/stations) |
| [Get Air Pollution Forecast](actions/get-air-pollution-forecast.md) | `GET /data/2.5/air_pollution/forecast` | [docs](https://openweathermap.org/api/air-pollution) |
| [Get Air Pollution History](actions/get-air-pollution-history.md) | `GET /data/2.5/air_pollution/history` | [docs](https://openweathermap.org/api/air-pollution) |
| [Get Climatic Forecast](actions/get-climatic-forecast.md) | `GET /data/2.5/forecast/climate` | [docs](https://openweathermap.org/api/forecast30) |
| [Get Climatic Forecast by City ID](actions/get-climatic-forecast-by-city-id.md) | `GET /data/2.5/forecast/climate` | [docs](https://openweathermap.org/api/forecast30) |
| [Get Climatic Forecast by City Name](actions/get-climatic-forecast-by-city-name.md) | `GET /data/2.5/forecast/climate` | [docs](https://openweathermap.org/api/forecast30) |
| [Get Climatic Forecast by ZIP](actions/get-climatic-forecast-by-zip.md) | `GET /data/2.5/forecast/climate` | [docs](https://openweathermap.org/api/forecast30) |
| [Get Current Air Pollution](actions/get-current-air-pollution.md) | `GET /data/2.5/air_pollution` | [docs](https://openweathermap.org/api/air-pollution) |
| [Get Current Weather](actions/get-current-weather.md) | `GET /data/2.5/weather` | [docs](https://openweathermap.org/current) |
| [Get Current Weather by City ID](actions/get-current-weather-by-city-id.md) | `GET /data/2.5/weather` | [docs](https://openweathermap.org/current) |
| [Get Current Weather by City Name](actions/get-current-weather-by-city-name.md) | `GET /data/2.5/weather` | [docs](https://openweathermap.org/current) |
| [Get Current Weather by ZIP](actions/get-current-weather-by-zip.md) | `GET /data/2.5/weather` | [docs](https://openweathermap.org/current) |
| [Get Daily Forecast](actions/get-daily-forecast.md) | `GET /data/2.5/forecast/daily` | [docs](https://openweathermap.org/forecast16) |
| [Get Daily Forecast by City ID](actions/get-daily-forecast-by-city-id.md) | `GET /data/2.5/forecast/daily` | [docs](https://openweathermap.org/forecast16) |
| [Get Daily Forecast by City Name](actions/get-daily-forecast-by-city-name.md) | `GET /data/2.5/forecast/daily` | [docs](https://openweathermap.org/forecast16) |
| [Get Daily Forecast by ZIP](actions/get-daily-forecast-by-zip.md) | `GET /data/2.5/forecast/daily` | [docs](https://openweathermap.org/forecast16) |
| [Get Fire Weather Index](actions/get-fire-weather-index.md) | `GET https://api.openweathermap.org/data/2.5/fwi` | [docs](https://openweathermap.org/api/fire-index-api) |
| [Get Fire Weather Index Forecast](actions/get-fire-weather-index-forecast.md) | `GET https://api.openweathermap.org/data/2.5/fwi/forecast` | [docs](https://openweathermap.org/api/fire-index-api) |
| [Get Fire Weather Map Tile](actions/get-fire-weather-map-tile.md) | `GET https://maps.openweathermap.org/maps/2.0/fwi/:z/:x/:y` | [docs](https://openweathermap.org/api/fire-index-map) |
| [Get 5 Day Forecast](actions/get-five-day-forecast.md) | `GET /data/2.5/forecast` | [docs](https://openweathermap.org/forecast5) |
| [Get 5 Day Forecast by City ID](actions/get-five-day-forecast-by-city-id.md) | `GET /data/2.5/forecast` | [docs](https://openweathermap.org/forecast5) |
| [Get 5 Day Forecast by City Name](actions/get-five-day-forecast-by-city-name.md) | `GET /data/2.5/forecast` | [docs](https://openweathermap.org/forecast5) |
| [Get 5 Day Forecast by ZIP](actions/get-five-day-forecast-by-zip.md) | `GET /data/2.5/forecast` | [docs](https://openweathermap.org/forecast5) |
| [Get Historical Weather](actions/get-historical-weather.md) | `GET https://history.openweathermap.org/data/2.5/history/city` | [docs](https://old.openweathermap.org/history) |
| [Get Hourly Forecast](actions/get-hourly-forecast.md) | `GET /data/2.5/forecast/hourly` | [docs](https://openweathermap.org/api/hourly-forecast) |
| [Get Hourly Forecast by City ID](actions/get-hourly-forecast-by-city-id.md) | `GET /data/2.5/forecast/hourly` | [docs](https://openweathermap.org/api/hourly-forecast) |
| [Get Hourly Forecast by City Name](actions/get-hourly-forecast-by-city-name.md) | `GET /data/2.5/forecast/hourly` | [docs](https://openweathermap.org/api/hourly-forecast) |
| [Get Hourly Forecast by ZIP](actions/get-hourly-forecast-by-zip.md) | `GET /data/2.5/forecast/hourly` | [docs](https://openweathermap.org/api/hourly-forecast) |
| [Get One Call Daily Summary](actions/get-one-call-daily-summary.md) | `GET /data/3.0/onecall/day_summary` | [docs](https://openweathermap.org/api/one-call-3) |
| [Get One Call Time Machine](actions/get-one-call-time-machine.md) | `GET /data/3.0/onecall/timemachine` | [docs](https://openweathermap.org/api/one-call-3) |
| [Get One Call Weather](actions/get-one-call-weather.md) | `GET /data/3.0/onecall` | [docs](https://openweathermap.org/api/one-call-3) |
| [Get Solar Interval Data](actions/get-solar-interval-data.md) | `GET https://api.openweathermap.org/energy/2.0/location/:locationId/interval_data` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Get Solar Location](actions/get-solar-location.md) | `GET https://api.openweathermap.org/energy/2.0/location/:locationId` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Get Solar Panel](actions/get-solar-panel.md) | `GET https://api.openweathermap.org/energy/2.0/panel/:panelId` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [Get Statistical Weather by Day](actions/get-statistical-weather-by-day.md) | `GET https://history.openweathermap.org/data/2.5/aggregated/day` | [docs](https://old.openweathermap.org/api/statistics-api) |
| [Get Statistical Weather by Month](actions/get-statistical-weather-by-month.md) | `GET https://history.openweathermap.org/data/2.5/aggregated/month` | [docs](https://old.openweathermap.org/api/statistics-api) |
| [Get Statistical Weather by Year](actions/get-statistical-weather-by-year.md) | `GET https://history.openweathermap.org/data/2.5/aggregated/year` | [docs](https://old.openweathermap.org/api/statistics-api) |
| [Get Weather Map Tile](actions/get-weather-map-tile.md) | `GET https://tile.openweathermap.org/map/:layer/:z/:x/:y.png` | [docs](https://openweathermap.org/api/weathermaps) |
| [Get Weather Overview](actions/get-weather-overview.md) | `GET /data/3.0/onecall/overview` | [docs](https://openweathermap.org/api/one-call-3) |
| [Get Weather Station](actions/get-weather-station.md) | `GET /data/3.0/stations/:stationId` | [docs](https://openweathermap.org/stations) |
| [List Solar Locations](actions/list-solar-locations.md) | `GET https://api.openweathermap.org/energy/2.0/locations` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [List Solar Panels](actions/list-solar-panels.md) | `GET https://api.openweathermap.org/energy/2.0/location/:locationId/panels` | [docs](https://openweathermap.org/api/solar-panels-and-energy-prediction-2) |
| [List Weather Stations](actions/list-weather-stations.md) | `GET /data/3.0/stations` | [docs](https://openweathermap.org/stations) |
| [Resume AI Weather Session](actions/resume-ai-weather-session.md) | `POST /assistant/session/:sessionId` | [docs](https://openweathermap.org/api/one-call-3) |
| [Reverse Geocode Coordinates](actions/reverse-geocode-coordinates.md) | `GET /geo/1.0/reverse` | [docs](https://openweathermap.org/api/geocoding-api) |
| [Start AI Weather Session](actions/start-ai-weather-session.md) | `POST /assistant/session` | [docs](https://openweathermap.org/api/one-call-3) |
| [Update Weather Station](actions/update-weather-station.md) | `PUT /data/3.0/stations/:stationId` | [docs](https://openweathermap.org/stations) |
| [Upload Weather Station Measurements](actions/upload-weather-station-measurements.md) | `POST /data/3.0/measurements` | [docs](https://openweathermap.org/stations) |
