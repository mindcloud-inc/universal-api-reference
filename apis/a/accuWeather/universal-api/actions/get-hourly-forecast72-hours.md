# AccuWeather: Get Hourly Forecast 72 Hours

Retrieves a 72-hour hourly forecast from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-hourly-forecast72-hours
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-hourly-forecast72-hours?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-hourly-forecast72-hours?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationKey` | string | yes | Required AccuWeather location key. Default: `349727`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DateTime": "string",
      "IconPhrase": "string",
      "IsDaylight": true,
      "Temperature": {
        "Value": 1
      },
      "WeatherIcon": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DateTime` | string |  |
| `IconPhrase` | string |  |
| `IsDaylight` | boolean |  |
| `Temperature.Value` | number |  |
| `WeatherIcon` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /forecasts/v1/hourly/72hour/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hourly-forecast72-hours.md) for the provider-specific parameters and requirements.

