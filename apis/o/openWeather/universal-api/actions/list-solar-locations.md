# OpenWeather: List Solar Locations

Lists solar locations in OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/list-solar-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "coordinates": {},
      "location_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coordinates` | object |  |
| `location_id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://api.openweathermap.org/energy/2.0/locations` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-solar-locations.md) for the provider-specific parameters and requirements.

