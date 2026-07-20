# <img src="https://images.mindcloud.co/apps/icons/pirate-weather_1775769177095.png" alt="Pirate Weather logo" width="28" height="28"> Pirate Weather: Universal API

Get weather forecasts and current conditions with Pirate Weather

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pirateWeather/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docs.pirateweather.net/en/latest/
- **Vendor API docs:** https://docs.pirateweather.net/en/latest/API/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Forecast](actions/get-forecast.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirateWeather/latest/actions/get-forecast?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Currentconditions

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Conditions](actions/get-current-conditions.md) | GET | Retrieves current conditions from Pirate Weather. |

### Dailyforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Forecast](actions/get-daily-forecast.md) | GET | Retrieves a daily forecast from Pirate Weather. |

### Daynightforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Day/Night Forecast](actions/get-day-night-forecast.md) | GET | Retrieves a day and night forecast from Pirate Weather. |

### Extendedhourlyforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Extended Hourly Forecast](actions/get-extended-hourly-forecast.md) | GET | Retrieves an extended hourly forecast from Pirate Weather. |

### Forecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Forecast](actions/get-forecast.md) | GET | Retrieves a weather forecast from Pirate Weather. |
| [Get Forecast With Extra Fields](actions/get-forecast-with-extra-fields.md) | GET | Retrieves a forecast with extra fields from Pirate Weather. |

### Historicalcurrentconditions

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Current Conditions](actions/get-historical-current-conditions.md) | GET | Retrieves historical current conditions from Pirate Weather. |

### Historicaldailyweather

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Daily Weather](actions/get-historical-daily-weather.md) | GET | Retrieves historical daily weather from Pirate Weather. |

### Historicalhourlyweather

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Hourly Weather](actions/get-historical-hourly-weather.md) | GET | Retrieves historical hourly weather from Pirate Weather. |

### Historicalweather

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Detailed Weather](actions/get-historical-detailed-weather.md) | GET | Retrieves detailed historical weather from Pirate Weather. |
| [Get Historical Weather](actions/get-historical-weather.md) | GET | Retrieves historical weather from Pirate Weather. |

### Hourlyforecast

| Action | Method | Description |
| --- | --- | --- |
| [Get Hourly Forecast](actions/get-hourly-forecast.md) | GET | Retrieves an hourly forecast from Pirate Weather. |

### Weatheralerts

| Action | Method | Description |
| --- | --- | --- |
| [Get Weather Alerts](actions/get-weather-alerts.md) | GET | Retrieves weather alerts from Pirate Weather. |

