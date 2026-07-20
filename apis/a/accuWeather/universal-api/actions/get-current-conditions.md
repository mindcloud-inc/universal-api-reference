# AccuWeather: Get Current Conditions

Retrieves current conditions from AccuWeather for a location.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-current-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-current-conditions?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-current-conditions?${params}`, {
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
| `IsDayTime` | boolean | Whether observation is daytime. |
| `LocalObservationDateTime` | string | Observation timestamp. |
| `Temperature.Metric.Value` | number | Observed temperature in metric units. |
| `WeatherIcon` | number | AccuWeather weather icon number. |
| `WeatherText` | string | Localized weather description. |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /currentconditions/v1/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-conditions.md) for the provider-specific parameters and requirements.

