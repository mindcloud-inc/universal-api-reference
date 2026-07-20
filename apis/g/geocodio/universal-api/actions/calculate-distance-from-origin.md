# Geocodio: Calculate Distance From Origin

Retrieves distances from one origin in Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-from-origin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-from-origin?connectionId=$CONNECTION_ID&origin=38.8977%2C-77.0365%2CWhiteHouse&destinations%5B%5D=38.8895%2C-77.0353%2CWashingtonMonument" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "origin": "38.8977,-77.0365,WhiteHouse",
  "destinations[]": "38.8895,-77.0353,WashingtonMonument"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-from-origin?${params}`, {
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
| `origin` | string | yes | Origin coordinate or address. Example: `38.8977,-77.0365,WhiteHouse`. |
| `destinations[]` | array<string> | yes | Destination coordinates or addresses. Example: `38.8895,-77.0353,WashingtonMonument`. |
| `mode` | string | no | Distance calculation mode: driving or straightline. One of: `0`, `1`. Default: `straightline`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `units` | string | no | Distance units: miles or km. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destinations": [
        {
          "distanceKm": 1,
          "distanceMiles": 1,
          "durationSeconds": 1,
          "id": "string",
          "location": [
            1
          ],
          "query": "string"
        }
      ],
      "mode": "string",
      "origin": {
        "id": "string",
        "location": [
          1
        ],
        "query": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinations` | array<object> | Calculated destination distances. |
| `destinations[].distanceKm` | number | Distance in kilometers. |
| `destinations[].distanceMiles` | number | Distance in miles. |
| `destinations[].durationSeconds` | number | Travel duration in seconds for driving mode. |
| `destinations[].id` | string | Destination identifier when provided. |
| `destinations[].location` | array<number> | Destination coordinates as latitude and longitude. |
| `destinations[].query` | string | Original destination query. |
| `mode` | string | Distance calculation mode. |
| `origin` | object | Origin location metadata. |
| `origin.id` | string | Origin identifier when provided. |
| `origin.location` | array<number> | Origin coordinates as latitude and longitude. |
| `origin.query` | string | Original origin query. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /distance` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-distance-from-origin.md) for the provider-specific parameters and requirements.

