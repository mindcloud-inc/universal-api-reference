# AccuWeather: Native API Reference

A consolidated summary of AccuWeather's API configuration and 64 documented operations, with links to official documentation.

- **Official docs:** https://developer.accuweather.com/documentation/overview
- **API base URL:** `https://dataservice.accuweather.com`

## Authentication

### API Key

Use your AccuWeather API key. AccuWeather requires Authorization: Bearer YOUR_API_KEY on requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.accuweather.com/documentation/authentication)

## Endpoints (64 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Cities](actions/autocomplete-cities.md) | `GET /locations/v1/cities/autocomplete` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [Autocomplete Points Of Interest](actions/autocomplete-points-of-interest.md) | `GET /locations/v1/pois/autocomplete` | [docs](https://developer.accuweather.com/core-weather/autocomplete-search) |
| [Get Alarm 1 Day](actions/get-alarm1-day.md) | `GET /alarms/v1/1day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-alarms) |
| [Get Alarm 10 Days](actions/get-alarm10-days.md) | `GET /alarms/v1/10day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-alarms) |
| [Get Alarm 15 Days](actions/get-alarm15-days.md) | `GET /alarms/v1/15day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-alarms) |
| [Get Alarm 5 Days](actions/get-alarm5-days.md) | `GET /alarms/v1/5day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-alarms) |
| [Get Current Conditions](actions/get-current-conditions.md) | `GET /currentconditions/v1/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-current-conditions) |
| [Get Current Conditions History 24 Hours](actions/get-current-conditions-history24-hours.md) | `GET /currentconditions/v1/:locationKey/historical/24` | [docs](https://developer.accuweather.com/core-weather/24-hour-historical-current-conditions) |
| [Get Current Conditions History 6 Hours](actions/get-current-conditions-history6-hours.md) | `GET /currentconditions/v1/:locationKey/historical` | [docs](https://developer.accuweather.com/core-weather/6-hour-historical-current-conditions) |
| [Get Daily Forecast 1 Day](actions/get-daily-forecast1-day.md) | `GET /forecasts/v1/daily/1day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-daily) |
| [Get Daily Forecast 10 Days](actions/get-daily-forecast10-days.md) | `GET /forecasts/v1/daily/10day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-daily) |
| [Get Daily Forecast 15 Days](actions/get-daily-forecast15-days.md) | `GET /forecasts/v1/daily/15day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-daily) |
| [Get Daily Forecast 5 Days](actions/get-daily-forecast5-days.md) | `GET /forecasts/v1/daily/5day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-daily) |
| [Get Daily Forecast 7 Days](actions/get-daily-forecast7-days.md) | `GET /forecasts/v1/daily/7day/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-daily) |
| [Get Daily Index Metadata](actions/get-daily-index-metadata.md) | `GET /indices/v1/daily/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get Hourly Forecast 1 Hour](actions/get-hourly-forecast1-hour.md) | `GET /forecasts/v1/hourly/1hour/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-hourly) |
| [Get Hourly Forecast 12 Hours](actions/get-hourly-forecast12-hours.md) | `GET /forecasts/v1/hourly/12hour/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-hourly) |
| [Get Hourly Forecast 120 Hours](actions/get-hourly-forecast120-hours.md) | `GET /forecasts/v1/hourly/120hour/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-hourly) |
| [Get Hourly Forecast 24 Hours](actions/get-hourly-forecast24-hours.md) | `GET /forecasts/v1/hourly/24hour/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-hourly) |
| [Get Hourly Forecast 72 Hours](actions/get-hourly-forecast72-hours.md) | `GET /forecasts/v1/hourly/72hour/:locationKey` | [docs](https://developer.accuweather.com/core-weather/location-key-hourly) |
| [Get Language Code By Id](actions/get-language-code-by-id.md) | `GET /translations/v1/languages/id/:languageID` | [docs](https://developer.accuweather.com/core-weather/languages-translations) |
| [Get Language Id By Code](actions/get-language-id-by-code.md) | `GET /translations/v1/languages/code/:languageCode` | [docs](https://developer.accuweather.com/core-weather/languages-translations) |
| [Get Location By Key](actions/get-location-by-key.md) | `GET /locations/v1/:locationKey` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [Get MinuteCast By Geoposition](actions/get-minute-cast-by-geoposition.md) | `GET /forecasts/v1/minute` | [docs](https://developer.accuweather.com/minutecast) |
| [Get Tropical Storm By Government Id](actions/get-tropical-storm-by-government-id.md) | `GET /tropical/v1/gov/storms/:year/:basin/:govId` | [docs](https://developer.accuweather.com/core-weather/active) |
| [Get Tropical Storm Forecasts](actions/get-tropical-storm-forecasts.md) | `GET /tropical/v1/gov/storms/:year/:basin/:govId/forecasts` | [docs](https://developer.accuweather.com/core-weather/forecast-tropical) |
| [Get Radar And Satellite Imagery 1024](actions/get-tropical-storm-images1024.md) | `GET /imagery/v1/maps/radsat/:resolution/:locationKey` | [docs](https://developer.accuweather.com/core-weather/imagery) |
| [Get Radar And Satellite Imagery 480](actions/get-tropical-storm-images480.md) | `GET /imagery/v1/maps/radsat/:resolution/:locationKey` | [docs](https://developer.accuweather.com/core-weather/imagery) |
| [Get Radar And Satellite Imagery 640](actions/get-tropical-storm-images640.md) | `GET /imagery/v1/maps/radsat/:resolution/:locationKey` | [docs](https://developer.accuweather.com/core-weather/imagery) |
| [Get Weather Alerts](actions/get-weather-alerts.md) | `GET /alerts/v1/:locationKey` | [docs](https://developer.accuweather.com/core-weather/weather-alerts) |
| [Get 1 Day Indices All](actions/get1-day-indices-all.md) | `GET /indices/v1/daily/1day/:locationKey` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 1 Day Indices Group](actions/get1-day-indices-group.md) | `GET /indices/v1/daily/1day/:locationKey/groups/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 1 Day Specific Index](actions/get1-day-specific-index.md) | `GET /indices/v1/daily/1day/:locationKey/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 10 Day Indices All](actions/get10-day-indices-all.md) | `GET /indices/v1/daily/10day/:locationKey` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 10 Day Indices Group](actions/get10-day-indices-group.md) | `GET /indices/v1/daily/10day/:locationKey/groups/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 10 Day Specific Index](actions/get10-day-specific-index.md) | `GET /indices/v1/daily/10day/:locationKey/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 15 Day Indices All](actions/get15-day-indices-all.md) | `GET /indices/v1/daily/15day/:locationKey` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 15 Day Indices Group](actions/get15-day-indices-group.md) | `GET /indices/v1/daily/15day/:locationKey/groups/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 15 Day Specific Index](actions/get15-day-specific-index.md) | `GET /indices/v1/daily/15day/:locationKey/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 5 Day Indices All](actions/get5-day-indices-all.md) | `GET /indices/v1/daily/5day/:locationKey` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 5 Day Indices Group](actions/get5-day-indices-group.md) | `GET /indices/v1/daily/5day/:locationKey/groups/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [Get 5 Day Specific Index](actions/get5-day-specific-index.md) | `GET /indices/v1/daily/5day/:locationKey/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [List Active Tropical Storms By Basin](actions/list-active-tropical-storms-by-basin.md) | `GET /tropical/v1/gov/storms/active/:basin` | [docs](https://developer.accuweather.com/core-weather/active) |
| [List Admin Areas By Country](actions/list-admin-areas-by-country.md) | `GET /locations/v1/adminareas/:countryCode` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [List Countries By Region](actions/list-countries-by-region.md) | `GET /locations/v1/countries/:regionCode` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [List Current Conditions For Top Cities](actions/list-current-conditions-for-top-cities.md) | `GET /currentconditions/v1/topcities/:group` | [docs](https://developer.accuweather.com/core-weather/top-cities-current-conditions) |
| [List Daily Indices Metadata](actions/list-daily-indices-metadata.md) | `GET /indices/v1/daily` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [List Index Groups](actions/list-index-groups.md) | `GET /indices/v1/daily/groups` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [List Indices In Group](actions/list-indices-in-group.md) | `GET /indices/v1/daily/groups/:ID` | [docs](https://developer.accuweather.com/accuweather-indices-api/apis) |
| [List Neighbor Cities](actions/list-neighbor-cities.md) | `GET /locations/v1/cities/neighbors/:locationKey` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [List Regions](actions/list-regions.md) | `GET /locations/v1/regions` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [List Supported Languages](actions/list-supported-languages.md) | `GET /translations/v1/languages` | [docs](https://developer.accuweather.com/core-weather/groups-translations) |
| [List Top Cities](actions/list-top-cities.md) | `GET /locations/v1/topcities/:group` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [List Translation Groups](actions/list-translation-groups.md) | `GET /translations/v1/groups` | [docs](https://developer.accuweather.com/core-weather/languages-translations) |
| [List Translations By Group Id](actions/list-translations-by-group-id.md) | `GET /translations/v1/groups/:groupID` | [docs](https://developer.accuweather.com/core-weather/languages-translations) |
| [Search Admin Areas By Country](actions/search-admin-areas-by-country.md) | `GET /locations/v1/adminareas/:countryCode/search` | [docs](https://developer.accuweather.com/core-weather/text-search) |
| [Search Admin Areas Globally](actions/search-admin-areas-globally.md) | `GET /locations/v1/adminareas/search` | [docs](https://developer.accuweather.com/core-weather/text-search) |
| [Search Cities](actions/search-cities.md) | `GET /locations/v1/cities/search` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [Search Cities By Country](actions/search-cities-by-country.md) | `GET /locations/v1/cities/:countryCode/search` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [Search Cities By Country And Admin Area](actions/search-cities-by-country-and-admin-area.md) | `GET /locations/v1/cities/:countryCode/:adminCode/search` | [docs](https://developer.accuweather.com/accuweather-locations-api/apis) |
| [Search Locations Globally](actions/search-locations-globally.md) | `GET /locations/v1/search` | [docs](https://developer.accuweather.com/core-weather/text-search) |
| [Search Points Of Interest](actions/search-points-of-interest.md) | `GET /locations/v1/pois/search` | [docs](https://developer.accuweather.com/core-weather/point-of-interest-search) |
| [Search Postal Codes](actions/search-postal-codes.md) | `GET /locations/v1/postalcodes/search` | [docs](https://developer.accuweather.com/core-weather/postal-code-search) |
| [Search Regions](actions/search-regions.md) | `GET /locations/v1/regions/:regionCode` | [docs](https://developer.accuweather.com/core-weather/text-search) |
