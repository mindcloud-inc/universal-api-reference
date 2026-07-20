# <img src="https://images.mindcloud.co/apps/icons/vaisala-xweather-api_1774900768765.png" alt="Vaisala Xweather logo" width="28" height="28"> Vaisala Xweather: Universal API

Get weather, forecast, alert, air quality, lightning, maritime, road weather, and environmental data from the Vaisala Xweather Weather API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vaisalaXweatherAPI/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.xweather.com/
- **Vendor API docs:** https://www.xweather.com/docs/weather-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Place](actions/get-place.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-place?connectionId=$CONNECTION_ID&id=seattle%2Cwa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Summaries Within Area](actions/get-alert-summaries-within-area.md) | GET | Retrieves alert summaries within an area from Vaisala Xweather API. |
| [Get Alert Summary](actions/get-alert-summary.md) | GET | Retrieves alert summary data from Vaisala Xweather API. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alerts from Vaisala Xweather API. |
| [Search Alert Summaries](actions/search-alert-summaries.md) | GET | Finds alert summaries in Vaisala Xweather API. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Air Quality Index](actions/get-air-quality-index.md) | GET | Retrieves air quality index data from Vaisala Xweather API. |
| [Get Air Quality Index Along Route](actions/get-air-quality-index-along-route.md) | GET | Retrieves air quality index data along a route from Vaisala Xweather API. |
| [Get Conditions Along Route](actions/get-conditions-along-route.md) | GET | Retrieves conditions along a route from Vaisala Xweather API. |
| [Get Conditions Summary](actions/get-conditions-summary.md) | GET | Retrieves conditions summary data from Vaisala Xweather API. |
| [Get Current Conditions](actions/get-current-conditions.md) | GET | Retrieves current conditions from Vaisala Xweather API. |
| [Get Current Observations](actions/get-current-observations.md) | GET | Retrieves current observations from Vaisala Xweather API. |
| [Get Forecast](actions/get-forecast.md) | GET | Retrieves forecast data from Vaisala Xweather API. |
| [Get Forecast Along Route](actions/get-forecast-along-route.md) | GET | Retrieves forecast data along a route from Vaisala Xweather API. |
| [Get Observation Summary](actions/get-observation-summary.md) | GET | Retrieves observation summary data from Vaisala Xweather API. |
| [Get Observations Along Route](actions/get-observations-along-route.md) | GET | Retrieves observations along a route from Vaisala Xweather API. |
| [Get Place](actions/get-place.md) | GET | Retrieves place details from Vaisala Xweather API. |
| [List Archived Observations](actions/list-archived-observations.md) | GET | Retrieves archived observations from Vaisala Xweather API. |
| [List Archived Observations Within Area](actions/list-archived-observations-within-area.md) | GET | Retrieves archived observations within an area from Vaisala Xweather API. |
| [List Closest Archived Observations](actions/list-closest-archived-observations.md) | GET | Retrieves closest archived observations from Vaisala Xweather API. |
| [List Closest Observations](actions/list-closest-observations.md) | GET | Retrieves closest observations from Vaisala Xweather API. |
| [List Closest Places](actions/list-closest-places.md) | GET | Retrieves closest places from Vaisala Xweather API. |
| [List Observations Within Area](actions/list-observations-within-area.md) | GET | Retrieves observations within an area from Vaisala Xweather API. |
| [List Places Within Area](actions/list-places-within-area.md) | GET | Retrieves places within an area from Vaisala Xweather API. |
| [Search Observations](actions/search-observations.md) | GET | Finds observations in Vaisala Xweather API. |
| [Search Places](actions/search-places.md) | GET | Finds places in Vaisala Xweather API. |

