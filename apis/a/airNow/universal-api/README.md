# <img src="https://images.mindcloud.co/apps/icons/airnow-icon_1775761501688.png" alt="AirNow logo" width="28" height="28"> AirNow: Universal API

Access AirNow air quality forecasts, current observations, historical observations, and monitoring-site data for reporting areas across the United States.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airNow/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.airnowapi.org/
- **Vendor API docs:** https://docs.airnowapi.org/webservices

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Current Observations by Zip Code](actions/list-current-observations-by-zip-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airNow/latest/actions/list-current-observations-by-zip-code?connectionId=$CONNECTION_ID&zipCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [List Monitoring Site Observations](actions/list-monitoring-site-observations.md) | GET | Retrieves monitoring site observations from AirNow within a geographic area. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [List Current Observations by Latitude Longitude](actions/list-current-observations-by-latitude-longitude.md) | GET | Retrieves current air quality observations from AirNow by latitude and longitude. |
| [List Current Observations by Zip Code](actions/list-current-observations-by-zip-code.md) | GET | Retrieves current air quality observations from AirNow by zip code. |
| [List Forecasts by Latitude Longitude](actions/list-forecasts-by-latitude-longitude.md) | GET | Retrieves air quality forecasts from AirNow by latitude and longitude. |
| [List Forecasts by Zip Code](actions/list-forecasts-by-zip-code.md) | GET | Retrieves air quality forecasts from AirNow by zip code. |
| [List Historical Observations by Latitude Longitude](actions/list-historical-observations-by-latitude-longitude.md) | GET | Retrieves historical air quality observations from AirNow by latitude and longitude. |
| [List Historical Observations by Zip Code](actions/list-historical-observations-by-zip-code.md) | GET | Retrieves historical air quality observations from AirNow by zip code. |

