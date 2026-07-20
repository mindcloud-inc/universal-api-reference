# <img src="https://images.mindcloud.co/apps/icons/iqair-airvisual-icon_1776185541017.png" alt="IQAir AirVisual logo" width="28" height="28"> IQAir AirVisual: Universal API

Access IQAir AirVisual v2 air-quality and weather data, including supported countries, states, cities, city observations, nearest-city observations, station lookup, station observations, nearest-station observations, and global city ranking where available for the connected API plan.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iQAirAirVisual/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.iqair.com/
- **Vendor API docs:** https://api-docs.iqair.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iQAirAirVisual/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get City Air Quality](actions/get-city-air-quality.md) | GET |  |
| [Get City Ranking](actions/get-city-ranking.md) | GET |  |
| [Get Nearest City Air Quality](actions/get-nearest-city-air-quality.md) | GET |  |
| [Get Nearest City Air Quality By IP](actions/get-nearest-city-air-quality-by-ip.md) | GET |  |
| [Get Nearest Station Air Quality](actions/get-nearest-station-air-quality.md) | GET |  |
| [Get Nearest Station Air Quality By IP](actions/get-nearest-station-air-quality-by-ip.md) | GET |  |
| [Get Station Air Quality](actions/get-station-air-quality.md) | GET |  |
| [List Cities](actions/list-cities.md) | GET |  |
| [List Countries](actions/list-countries.md) | GET |  |
| [List States](actions/list-states.md) | GET |  |
| [List Stations](actions/list-stations.md) | GET |  |

