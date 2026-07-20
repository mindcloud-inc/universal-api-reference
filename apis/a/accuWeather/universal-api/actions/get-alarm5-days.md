# AccuWeather: Get Alarm 5 Days

Retrieves 5-day weather alarms from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-alarm5-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-alarm5-days?connectionId=$CONNECTION_ID&locationKey=349727" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-alarm5-days?${params}`, {
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
      "Day": 1,
      "Name": "Ava Chen",
      "Type": "string",
      "Value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Day` | number |  |
| `Name` | string |  |
| `Type` | string |  |
| `Value` | number |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /alarms/v1/5day/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alarm5-days.md) for the provider-specific parameters and requirements.

