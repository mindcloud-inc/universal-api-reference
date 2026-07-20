# OpenWeather: Get Weather Map Tile

Retrieves a weather map tile from OpenWeather.

```
GET https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-map-tile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-map-tile?connectionId=$CONNECTION_ID&apiKey=string&layer=string&x=string&y=string&z=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKey": "string",
  "layer": "string",
  "x": "string",
  "y": "string",
  "z": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/get-weather-map-tile?${params}`, {
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
| `layer` | string | yes | Map layer code. |
| `x` | string | yes | Tile X coordinate. |
| `y` | string | yes | Tile Y coordinate. |
| `z` | string | yes | Tile zoom level. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "layer": "string",
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
| `layer` | string |  |
| `tileUrl` | string |  |
| `x` | string |  |
| `y` | string |  |
| `z` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `GET https://tile.openweathermap.org/map/:layer/:z/:x/:y.png` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weather-map-tile.md) for the provider-specific parameters and requirements.

