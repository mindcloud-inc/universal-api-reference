# <img src="https://images.mindcloud.co/apps/icons/wttrin_1777583700550.png" alt="wttr.in logo" width="28" height="28"> wttr.in: Universal API

Fetch forecasts, current conditions, metrics, and moon phases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wttrin/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wttr.in
- **Vendor API docs:** https://github.com/chubin/wttr.in

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Weather Forecast JSON](actions/get-weather-forecast-json.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-forecast-json?connectionId=$CONNECTION_ID&location=London" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Compact Weather Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Compact Weather Forecast JSON](actions/get-compact-weather-forecast-json.md) | GET | Retrieves compact weather forecast JSON from wttr.in. |

### Current Weather Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Weather Summary](actions/get-current-weather-summary.md) | GET | Retrieves the current weather summary from wttr.in. |

### Moon Phase

| Action | Method | Description |
| --- | --- | --- |
| [Get Moon Phase](actions/get-moon-phase.md) | GET | Retrieves the moon phase for a date from wttr.in. |

### Weather Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Forecast JSON](actions/get-weather-forecast-json.md) | GET | Retrieves full weather forecast JSON from wttr.in. |

### Weather Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Metrics](actions/get-weather-metrics.md) | GET | Retrieves Prometheus weather metrics from wttr.in. |

