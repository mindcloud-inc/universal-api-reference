# OpenWeather: Get Fire Weather Map Tile

Retrieves a fire weather map tile from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-map-tile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-map-tile?connectionId=$CONNECTION_ID&apiKey=string&x=string&y=string&z=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKey": "string",
  "x": "string",
  "y": "string",
  "z": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-fire-weather-map-tile?${params}`, {
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
| `apiKey` | string | yes | OpenWeather API key injected from the app connection. |
| `date` | string | no | Map date timestamp when required by provider contract. |
| `x` | string | yes | Tile X coordinate. |
| `y` | string | yes | Tile Y coordinate. |
| `z` | string | yes | Tile zoom level. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "tileUrl": "https://example.com",
      "x": "string",
      "y": "string",
      "z": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `tileUrl` | string |  |
| `x` | string |  |
| `y` | string |  |
| `z` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://maps.openweathermap.org/maps/2.0/fwi/:z/:x/:y` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fire-weather-map-tile.md) for the provider-specific parameters and requirements.

