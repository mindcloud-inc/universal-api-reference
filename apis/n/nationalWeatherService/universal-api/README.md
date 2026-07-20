# <img src="https://images.mindcloud.co/apps/icons/us-national-weather-service-logo_1777501848143.png" alt="National Weather Service logo" width="28" height="28"> National Weather Service: Universal API

Access forecasts, alerts, observations, and weather data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nationalWeatherService/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.weather.gov
- **Vendor API docs:** https://www.weather.gov/documentation/services-web-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Alert Types](actions/list-alert-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/list-alert-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Active Alert Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Active Alerts](actions/count-active-alerts.md) | GET | Retrieves active alert counts from National Weather Service. |

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | GET | Retrieves an alert from National Weather Service. |
| [List Active Alerts](actions/list-active-alerts.md) | GET | Retrieves active alerts from National Weather Service. |
| [List Active Alerts By Area](actions/list-active-alerts-by-area.md) | GET | Retrieves active alerts from National Weather Service by area. |
| [List Active Alerts By Marine Region](actions/list-active-alerts-by-marine-region.md) | GET | Retrieves active alerts from National Weather Service by marine region. |
| [List Active Alerts By Zone](actions/list-active-alerts-by-zone.md) | GET | Retrieves active alerts from National Weather Service by zone. |
| [Query Alerts](actions/query-alerts.md) | GET | Retrieves alerts from National Weather Service. |

### Alert Type

| Action | Method | Description |
| --- | --- | --- |
| [List Alert Types](actions/list-alert-types.md) | GET | Retrieves alert types from National Weather Service. |

### Center Weather Advisory

| Action | Method | Description |
| --- | --- | --- |
| [List Center Weather Advisories](actions/list-center-weather-advisories.md) | GET | Retrieves center weather advisories from National Weather Service. |

### Forecast Office

| Action | Method | Description |
| --- | --- | --- |
| [Get Forecast Office](actions/get-forecast-office.md) | GET | Retrieves a forecast office from National Weather Service. |

### Gridpoint Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Gridpoint Forecast](actions/get-gridpoint-forecast.md) | GET | Retrieves the forecast for a National Weather Service gridpoint. |

### Gridpoint Hourly Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Gridpoint Hourly Forecast](actions/get-gridpoint-hourly-forecast.md) | GET | Retrieves the hourly forecast for a National Weather Service gridpoint. |

### Gridpoint Raw Forecast Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Gridpoint Raw Forecast Data](actions/get-gridpoint-raw-forecast-data.md) | GET | Retrieves raw forecast data for a National Weather Service gridpoint. |

### Observation Station

| Action | Method | Description |
| --- | --- | --- |
| [Get Observation Station](actions/get-observation-station.md) | GET | Retrieves an observation station from National Weather Service. |
| [List Gridpoint Observation Stations](actions/list-gridpoint-observation-stations.md) | GET | Retrieves observation stations for a National Weather Service gridpoint. |
| [List Observation Stations](actions/list-observation-stations.md) | GET | Retrieves observation stations from National Weather Service. |
| [List Point Observation Stations](actions/list-point-observation-stations.md) | GET | Retrieves observation stations for a National Weather Service point. |
| [List Zone Observation Stations](actions/list-zone-observation-stations.md) | GET | Retrieves observation stations for a National Weather Service zone. |

### Office Briefing

| Action | Method | Description |
| --- | --- | --- |
| [Get Office Briefing](actions/get-office-briefing.md) | GET | Retrieves an office briefing from National Weather Service. |

### Office Headline

| Action | Method | Description |
| --- | --- | --- |
| [Get Office Headline](actions/get-office-headline.md) | GET | Retrieves an office headline from National Weather Service. |
| [List Office Headlines](actions/list-office-headlines.md) | GET | Retrieves office headlines from National Weather Service. |

### Office Weather Story

| Action | Method | Description |
| --- | --- | --- |
| [Get Office Weather Stories](actions/get-office-weather-stories.md) | GET | Retrieves office weather stories from National Weather Service. |

### Point Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Resolve Point Metadata](actions/resolve-point-metadata.md) | GET | Retrieves point metadata from National Weather Service by coordinates. |

### Point Weather Radio Script

| Action | Method | Description |
| --- | --- | --- |
| [Get Point Weather Radio Script](actions/get-point-weather-radio-script.md) | GET | Retrieves the weather radio script for a National Weather Service point. |

### Sigmet Or Airmet

| Action | Method | Description |
| --- | --- | --- |
| [List SIGMETs And AIRMETs](actions/list-sigmets-and-airmets.md) | GET | Retrieves SIGMETs and AIRMETs from National Weather Service. |

### Station Observation

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Station Observation](actions/get-latest-station-observation.md) | GET | Retrieves the latest observation for a National Weather Service station. |
| [Get Station Observation By Time](actions/get-station-observation-by-time.md) | GET | Retrieves a station observation from National Weather Service by time. |
| [List Station Observations](actions/list-station-observations.md) | GET | Retrieves observations for a National Weather Service station. |

### Terminal Aerodrome Forecast

| Action | Method | Description |
| --- | --- | --- |
| [List Station TAFs](actions/list-station-tafs.md) | GET | Retrieves station TAFs from National Weather Service. |

### Text Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Product By Type And Location](actions/get-latest-product-by-type-and-location.md) | GET | Retrieves the latest text product from National Weather Service by type and location. |
| [Get Text Product](actions/get-text-product.md) | GET | Retrieves a text product from National Weather Service. |
| [List Products By Type](actions/list-products-by-type.md) | GET | Retrieves text products from National Weather Service by type. |
| [Search Text Products](actions/search-text-products.md) | GET | Retrieves text products from National Weather Service. |

### Text Product Location

| Action | Method | Description |
| --- | --- | --- |
| [List Text Product Locations](actions/list-text-product-locations.md) | GET | Retrieves text product locations from National Weather Service. |

### Text Product Type

| Action | Method | Description |
| --- | --- | --- |
| [List Text Product Types](actions/list-text-product-types.md) | GET | Retrieves text product types from National Weather Service. |

### Zone

| Action | Method | Description |
| --- | --- | --- |
| [Get Zone](actions/get-zone.md) | GET | Retrieves a zone from National Weather Service. |
| [List Zones](actions/list-zones.md) | GET | Retrieves zones from National Weather Service. |
| [List Zones By Type](actions/list-zones-by-type.md) | GET | Retrieves zones from National Weather Service by type. |

### Zone Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Zone Forecast](actions/get-zone-forecast.md) | GET | Retrieves a zone forecast from National Weather Service. |

### Zone Forecast Observation

| Action | Method | Description |
| --- | --- | --- |
| [List Zone Forecast Observations](actions/list-zone-forecast-observations.md) | GET | Retrieves observations for a National Weather Service forecast zone. |

