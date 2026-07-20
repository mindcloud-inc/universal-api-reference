# <img src="https://images.mindcloud.co/apps/icons/favicon-14_1775483013436.png" alt="Ambee logo" width="28" height="28"> Ambee: Universal API

Access climate, air quality, pollen, weather, wildfire, disaster, geocoding, and elevation data from Ambee.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ambee/latest
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getambee.com/
- **Vendor API docs:** https://docs.ambeedata.com/apis/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Geocode By Place](actions/geocode-by-place.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ambee/latest/actions/geocode-by-place?connectionId=$CONNECTION_ID&place=new%20york" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Air Quality

| Action | Method | Description |
| --- | --- | --- |
| [Get Air Quality Forecast By Coordinates](actions/get-air-quality-forecast-by-coordinates.md) | GET | Retrieves air quality forecasts in Ambee by coordinates. |
| [Get Latest Air Quality By City](actions/get-latest-air-quality-by-city.md) | GET | Retrieves latest air quality data in Ambee by city. |
| [Get Latest Air Quality By Coordinates](actions/get-latest-air-quality-by-coordinates.md) | GET | Retrieves latest air quality data in Ambee by coordinates. |
| [Get Latest Air Quality By Country Code](actions/get-latest-air-quality-by-country-code.md) | GET | Retrieves latest air quality data in Ambee by country code. |
| [Get Latest Air Quality By Postal Code](actions/get-latest-air-quality-by-postal-code.md) | GET | Retrieves latest air quality data in Ambee by postal code. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Geocode By Place](actions/geocode-by-place.md) | GET | Retrieves location coordinates in Ambee by place name. |
| [Reverse Geocode By Coordinates](actions/reverse-geocode-by-coordinates.md) | GET | Retrieves nearby location details in Ambee by coordinates. |

### Pollen

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Latest Pollen By Coordinates](actions/retrieve-latest-pollen-by-coordinates.md) | GET | Retrieves latest pollen data in Ambee by coordinates. |
| [Retrieve Latest Pollen By Place](actions/retrieve-latest-pollen-by-place.md) | GET | Retrieves latest pollen data in Ambee by place name. |
| [Retrieve Pollen Forecast By Coordinates](actions/retrieve-pollen-forecast-by-coordinates.md) | GET | Retrieves pollen forecasts in Ambee by coordinates. |
| [Retrieve Pollen Forecast By Place](actions/retrieve-pollen-forecast-by-place.md) | GET | Retrieves pollen forecasts in Ambee by place name. |
| [Retrieve Pollen 120hr Forecast By Coordinates](actions/retrieve-pollen120hr-forecast-by-coordinates.md) | GET | Retrieves 120-hour pollen forecasts in Ambee by coordinates. |
| [Retrieve Pollen 120hr Forecast By Place](actions/retrieve-pollen120hr-forecast-by-place.md) | GET | Retrieves 120-hour pollen forecasts in Ambee by place name. |

### Weather

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Latest Weather By Coordinates](actions/retrieve-latest-weather-by-coordinates.md) | GET | Retrieves latest weather data in Ambee by coordinates. |
| [Retrieve Weather Forecast By Coordinates](actions/retrieve-weather-forecast-by-coordinates.md) | GET | Retrieves weather forecasts in Ambee by coordinates. |

### Wildfire

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Wildfire By Coordinates](actions/get-latest-wildfire-by-coordinates.md) | GET | Retrieves latest wildfire data in Ambee by coordinates. |
| [Get Wildfire Forecast By Coordinates](actions/get-wildfire-forecast-by-coordinates.md) | GET | Retrieves wildfire risk forecasts in Ambee by coordinates. |
| [Retrieve Latest Wildfire By Place](actions/retrieve-latest-wildfire-by-place.md) | GET | Retrieves latest wildfire data in Ambee by place name. |
| [Retrieve Wildfire Forecast By Place](actions/retrieve-wildfire-forecast-by-place.md) | GET | Retrieves wildfire risk forecasts in Ambee by place name. |

