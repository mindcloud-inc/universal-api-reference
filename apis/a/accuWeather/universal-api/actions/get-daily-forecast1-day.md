# AccuWeather: Get Daily Forecast 1 Day

Retrieves a 1-day daily forecast from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-forecast1-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-forecast1-day?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-daily-forecast1-day?${params}`, {
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
      "DailyForecasts": {
        "Date": "string",
        "Day": {
          "IconPhrase": "string"
        },
        "Temperature": {
          "Maximum": {
            "Value": 1
          },
          "Minimum": {
            "Value": 1
          }
        }
      },
      "Headline": {
        "Text": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DailyForecasts.Date` | string |  |
| `DailyForecasts.Day.IconPhrase` | string |  |
| `DailyForecasts.Temperature.Maximum.Value` | number |  |
| `DailyForecasts.Temperature.Minimum.Value` | number |  |
| `Headline.Text` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /forecasts/v1/daily/1day/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-forecast1-day.md) for the provider-specific parameters and requirements.

