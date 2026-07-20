# National Weather Service: Resolve Point Metadata

Retrieves point metadata from National Weather Service by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/resolve-point-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Weather Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/resolve-point-metadata?connectionId=$CONNECTION_ID&latitude=39.7456&longitude=-97.0892" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "39.7456",
  "longitude": "-97.0892"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalWeatherService/latest/actions/resolve-point-metadata?${params}`, {
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
| `latitude` | number | yes | Latitude in decimal degrees. Example: `39.7456`. |
| `longitude` | number | yes | Longitude in decimal degrees. Example: `-97.0892`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "geometry": {},
      "id": "https://example.com",
      "properties": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `geometry` | object |  |
| `id` | string |  |
| `properties` | object |  |
| `type` | string |  |

## Native endpoint

Through the native National Weather Service API, this operation is `GET /points/:latitude,:longitude` (base URL `https://api.weather.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-point-metadata.md) for the provider-specific parameters and requirements.

