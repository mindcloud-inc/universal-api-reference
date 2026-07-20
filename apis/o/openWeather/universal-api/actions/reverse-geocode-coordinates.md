# OpenWeather: Reverse Geocode Coordinates

Finds OpenWeather locations by geographic coordinates.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/reverse-geocode-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/reverse-geocode-coordinates?connectionId=$CONNECTION_ID&lat=1&lon=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lon": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/reverse-geocode-coordinates?${params}`, {
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
| `lat` | number | yes | Latitude to reverse geocode. |
| `lon` | number | yes | Longitude to reverse geocode. |
| `limit` | number | no | Maximum number of nearby locations to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "lat": 1,
      "local_names": {},
      "lon": 1,
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `lat` | number |  |
| `local_names` | object |  |
| `lon` | number |  |
| `name` | string |  |
| `state` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET /geo/1.0/reverse` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-coordinates.md) for the provider-specific parameters and requirements.

