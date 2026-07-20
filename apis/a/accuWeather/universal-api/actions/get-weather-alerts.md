# AccuWeather: Get Weather Alerts

Retrieves weather alerts from AccuWeather for a location.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-weather-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-weather-alerts?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-weather-alerts?${params}`, {
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
      "AlertID": 1,
      "Category": "string",
      "Description": {
        "Localized": "string"
      },
      "Priority": 1,
      "Source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AlertID` | number |  |
| `Category` | string |  |
| `Description.Localized` | string |  |
| `Priority` | number |  |
| `Source` | string |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /alerts/v1/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weather-alerts.md) for the provider-specific parameters and requirements.

