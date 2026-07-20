# AccuWeather: List Current Conditions For Top Cities

Lists current conditions for top cities in AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-current-conditions-for-top-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-current-conditions-for-top-cities?connectionId=$CONNECTION_ID&group=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-current-conditions-for-top-cities?${params}`, {
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
| `group` | string | yes | Required top-city group number. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsDayTime": true,
      "LocalObservationDateTime": "string",
      "Temperature": {
        "Metric": {
          "Value": 1
        }
      },
      "WeatherIcon": 1,
      "WeatherText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsDayTime` | boolean |  |
| `LocalObservationDateTime` | string |  |
| `Temperature.Metric.Value` | number |  |
| `WeatherIcon` | number |  |
| `WeatherText` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /currentconditions/v1/topcities/:group` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-conditions-for-top-cities.md) for the provider-specific parameters and requirements.

