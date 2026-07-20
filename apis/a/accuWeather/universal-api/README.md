# <img src="https://images.mindcloud.co/apps/icons/accuweather-icon-square_1776182571781.png" alt="AccuWeather logo" width="28" height="28"> AccuWeather: Universal API

Official AccuWeather API integration for locations, current conditions, forecasts, alerts, alarms, imagery, tropical, translations, and MinuteCast data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/accuWeather/latest
- **Actions:** 64
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.accuweather.com
- **Vendor API docs:** https://developer.accuweather.com/documentation/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Languages](actions/list-supported-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (64)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Cities](actions/autocomplete-cities.md) | GET | Finds cities in AccuWeather by autocomplete text. |
| [Autocomplete Points Of Interest](actions/autocomplete-points-of-interest.md) | GET | Finds points of interest in AccuWeather by autocomplete. |
| [Get Alarm 1 Day](actions/get-alarm1-day.md) | GET | Retrieves 1-day weather alarms from AccuWeather. |
| [Get Alarm 10 Days](actions/get-alarm10-days.md) | GET | Retrieves 10-day weather alarms from AccuWeather. |
| [Get Alarm 15 Days](actions/get-alarm15-days.md) | GET | Retrieves 15-day weather alarms from AccuWeather. |
| [Get Alarm 5 Days](actions/get-alarm5-days.md) | GET | Retrieves 5-day weather alarms from AccuWeather. |
| [Get Current Conditions](actions/get-current-conditions.md) | GET | Retrieves current conditions from AccuWeather for a location. |
| [Get Current Conditions History 24 Hours](actions/get-current-conditions-history24-hours.md) | GET | Retrieves 24-hour current conditions history from AccuWeather. |
| [Get Current Conditions History 6 Hours](actions/get-current-conditions-history6-hours.md) | GET | Retrieves 6-hour current conditions history from AccuWeather. |
| [Get Daily Forecast 1 Day](actions/get-daily-forecast1-day.md) | GET | Retrieves a 1-day daily forecast from AccuWeather. |
| [Get Daily Forecast 10 Days](actions/get-daily-forecast10-days.md) | GET | Retrieves a 10-day daily forecast from AccuWeather. |
| [Get Daily Forecast 15 Days](actions/get-daily-forecast15-days.md) | GET | Retrieves a 15-day daily forecast from AccuWeather. |
| [Get Daily Forecast 5 Days](actions/get-daily-forecast5-days.md) | GET | Retrieves a 5-day daily forecast from AccuWeather. |
| [Get Daily Forecast 7 Days](actions/get-daily-forecast7-days.md) | GET | Retrieves a 7-day daily forecast from AccuWeather. |
| [Get Daily Index Metadata](actions/get-daily-index-metadata.md) | GET | Retrieves daily index metadata from AccuWeather. |
| [Get Hourly Forecast 1 Hour](actions/get-hourly-forecast1-hour.md) | GET | Retrieves a 1-hour hourly forecast from AccuWeather. |
| [Get Hourly Forecast 12 Hours](actions/get-hourly-forecast12-hours.md) | GET | Retrieves a 12-hour hourly forecast from AccuWeather. |
| [Get Hourly Forecast 120 Hours](actions/get-hourly-forecast120-hours.md) | GET | Retrieves a 120-hour hourly forecast from AccuWeather. |
| [Get Hourly Forecast 24 Hours](actions/get-hourly-forecast24-hours.md) | GET | Retrieves a 24-hour hourly forecast from AccuWeather. |
| [Get Hourly Forecast 72 Hours](actions/get-hourly-forecast72-hours.md) | GET | Retrieves a 72-hour hourly forecast from AccuWeather. |
| [Get Language Code By Id](actions/get-language-code-by-id.md) | GET | Retrieves a language code from AccuWeather by ID. |
| [Get Language Id By Code](actions/get-language-id-by-code.md) | GET | Retrieves a language ID from AccuWeather by code. |
| [Get Location By Key](actions/get-location-by-key.md) | GET | Retrieves a location from AccuWeather by key. |
| [Get MinuteCast By Geoposition](actions/get-minute-cast-by-geoposition.md) | GET | Retrieves MinuteCast data from AccuWeather by geoposition. |
| [Get Tropical Storm By Government Id](actions/get-tropical-storm-by-government-id.md) | GET | Retrieves a tropical storm from AccuWeather by year, basin, and government ID. |
| [Get Tropical Storm Forecasts](actions/get-tropical-storm-forecasts.md) | GET | Retrieves tropical storm forecasts from AccuWeather by year, basin, and government ID. |
| [Get Radar And Satellite Imagery 1024](actions/get-tropical-storm-images1024.md) | GET | Retrieves 1024px radar and satellite imagery from AccuWeather. |
| [Get Radar And Satellite Imagery 480](actions/get-tropical-storm-images480.md) | GET | Retrieves 480px radar and satellite imagery from AccuWeather. |
| [Get Radar And Satellite Imagery 640](actions/get-tropical-storm-images640.md) | GET | Retrieves 640px radar and satellite imagery from AccuWeather. |
| [Get Weather Alerts](actions/get-weather-alerts.md) | GET | Retrieves weather alerts from AccuWeather for a location. |
| [Get 1 Day Indices All](actions/get1-day-indices-all.md) | GET | Retrieves all 1-day indices from AccuWeather. |
| [Get 1 Day Indices Group](actions/get1-day-indices-group.md) | GET | Retrieves 1-day index groups from AccuWeather. |
| [Get 1 Day Specific Index](actions/get1-day-specific-index.md) | GET | Retrieves a 1-day specific index from AccuWeather. |
| [Get 10 Day Indices All](actions/get10-day-indices-all.md) | GET | Retrieves all 10-day indices from AccuWeather. |
| [Get 10 Day Indices Group](actions/get10-day-indices-group.md) | GET | Retrieves 10-day index groups from AccuWeather. |
| [Get 10 Day Specific Index](actions/get10-day-specific-index.md) | GET | Retrieves a 10-day specific index from AccuWeather. |
| [Get 15 Day Indices All](actions/get15-day-indices-all.md) | GET | Retrieves all 15-day indices from AccuWeather. |
| [Get 15 Day Indices Group](actions/get15-day-indices-group.md) | GET | Retrieves 15-day index groups from AccuWeather. |
| [Get 15 Day Specific Index](actions/get15-day-specific-index.md) | GET | Retrieves a 15-day specific index from AccuWeather. |
| [Get 5 Day Indices All](actions/get5-day-indices-all.md) | GET | Retrieves all 5-day indices from AccuWeather. |
| [Get 5 Day Indices Group](actions/get5-day-indices-group.md) | GET | Retrieves 5-day index groups from AccuWeather. |
| [Get 5 Day Specific Index](actions/get5-day-specific-index.md) | GET | Retrieves a 5-day specific index from AccuWeather. |
| [List Active Tropical Storms By Basin](actions/list-active-tropical-storms-by-basin.md) | GET | Lists active tropical storms in AccuWeather by basin. |
| [List Admin Areas By Country](actions/list-admin-areas-by-country.md) | GET | Lists the admin areas in AccuWeather for a country. |
| [List Countries By Region](actions/list-countries-by-region.md) | GET | Lists the countries in AccuWeather for a region. |
| [List Current Conditions For Top Cities](actions/list-current-conditions-for-top-cities.md) | GET | Lists current conditions for top cities in AccuWeather. |
| [List Daily Indices Metadata](actions/list-daily-indices-metadata.md) | GET | Lists daily indices metadata in AccuWeather. |
| [List Index Groups](actions/list-index-groups.md) | GET | Lists daily index groups in AccuWeather. |
| [List Indices In Group](actions/list-indices-in-group.md) | GET | Lists daily indices in an AccuWeather group. |
| [List Neighbor Cities](actions/list-neighbor-cities.md) | GET | Lists neighboring cities in AccuWeather for a location. |
| [List Regions](actions/list-regions.md) | GET | Lists the region records in AccuWeather. |
| [List Supported Languages](actions/list-supported-languages.md) | GET | Lists the supported languages in AccuWeather. |
| [List Top Cities](actions/list-top-cities.md) | GET | Lists top cities in AccuWeather by group. |
| [List Translation Groups](actions/list-translation-groups.md) | GET | Lists the translation groups in AccuWeather. |
| [List Translations By Group Id](actions/list-translations-by-group-id.md) | GET | Lists translations in AccuWeather for a group. |
| [Search Admin Areas By Country](actions/search-admin-areas-by-country.md) | GET | Finds admin areas in AccuWeather by country. |
| [Search Admin Areas Globally](actions/search-admin-areas-globally.md) | GET | Finds admin areas in AccuWeather by global search. |
| [Search Cities](actions/search-cities.md) | GET | Finds cities in AccuWeather by text search. |
| [Search Cities By Country](actions/search-cities-by-country.md) | GET | Finds cities in AccuWeather by country and text. |
| [Search Cities By Country And Admin Area](actions/search-cities-by-country-and-admin-area.md) | GET | Finds cities in AccuWeather by country and admin area. |
| [Search Locations Globally](actions/search-locations-globally.md) | GET | Finds locations in AccuWeather by global text search. |
| [Search Points Of Interest](actions/search-points-of-interest.md) | GET | Finds points of interest in AccuWeather by text. |
| [Search Postal Codes](actions/search-postal-codes.md) | GET | Finds locations in AccuWeather by postal code. |
| [Search Regions](actions/search-regions.md) | GET | Retrieves a region from AccuWeather by region code. |

