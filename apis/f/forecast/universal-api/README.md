# <img src="https://images.mindcloud.co/apps/icons/forecast_1774383074062.png" alt="Forecast logo" width="28" height="28"> Forecast: Universal API

Generate demand and time-series forecasts with ForecastAPI

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/forecast/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forecastapi.com
- **Vendor API docs:** https://forecastapi.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Forecast](actions/generate-forecast.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forecast/latest/actions/generate-forecast?connectionId=$CONNECTION_ID&identifier=SKU-12345&data=%5Bobject%20Object%5D&periods=6&frequency=M&data%5B%5D.date=2024-01-01&data%5B%5D.value=120" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Generate Forecast](actions/generate-forecast.md) | GET | Generates forecasts in Forecast. |
| [Generate Traffic Forecast](actions/generate-traffic-forecast.md) | GET | Generates traffic forecasts in Forecast. |

