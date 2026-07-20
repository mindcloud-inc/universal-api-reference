# OpenWeather: Get Solar Interval Data

Retrieves solar interval data from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-solar-interval-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-solar-interval-data?connectionId=$CONNECTION_ID&locationId=string&date=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string",
  "date": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-solar-interval-data?${params}`, {
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
| `locationId` | string | yes | Solar location identifier. |
| `date` | string | yes | Date to retrieve interval data for. |
| `interval` | string | yes | Requested interval granularity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "interval": "string",
      "intervals": [
        {}
      ],
      "lat": 1,
      "location_id": "string",
      "lon": 1,
      "tz": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `interval` | string |  |
| `intervals` | array<object> |  |
| `lat` | number |  |
| `location_id` | string |  |
| `lon` | number |  |
| `tz` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://api.openweathermap.org/energy/2.0/location/:locationId/interval_data` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-solar-interval-data.md) for the provider-specific parameters and requirements.

