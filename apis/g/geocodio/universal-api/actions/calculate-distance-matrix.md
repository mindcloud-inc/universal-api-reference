# Geocodio: Calculate Distance Matrix

Retrieves a distance matrix from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-matrix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-matrix?connectionId=$CONNECTION_ID&origins%5B%5D=38.8977%2C-77.0365%2CWhiteHouse&destinations%5B%5D=38.8895%2C-77.0353%2CWashingtonMonument" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "origins[]": "38.8977,-77.0365,WhiteHouse",
  "destinations[]": "38.8895,-77.0353,WashingtonMonument"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/calculate-distance-matrix?${params}`, {
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
| `origins[]` | array<string> | yes | Array of origin coordinates or addresses. Example: `38.8977,-77.0365,WhiteHouse`. |
| `destinations[]` | array<string> | yes | Array of destination coordinates or addresses. Example: `38.8895,-77.0353,WashingtonMonument`. |
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
      "mode": "string",
      "results": [
        {
          "destinations": [
            {
              "distanceKm": 1,
              "distanceMiles": 1,
              "durationSeconds": 1,
              "id": "string",
              "location": [
                1
              ]
            }
          ],
          "origin": {
            "id": "string",
            "location": [
              1
            ]
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mode` | string | Distance calculation mode. |
| `results` | array<object> | Distance matrix rows by origin. |
| `results[].destinations` | array<object> | Calculated destination distances for this origin. |
| `results[].destinations[].distanceKm` | number | Distance in kilometers. |
| `results[].destinations[].distanceMiles` | number | Distance in miles. |
| `results[].destinations[].durationSeconds` | number | Travel duration in seconds for driving mode. |
| `results[].destinations[].id` | string | Destination identifier when provided. |
| `results[].destinations[].location` | array<number> | Destination coordinates as latitude and longitude. |
| `results[].origin` | object | Origin location metadata. |
| `results[].origin.id` | string | Origin identifier when provided. |
| `results[].origin.location` | array<number> | Origin coordinates as latitude and longitude. |

## Native endpoint

Through the native Geocodio API, this operation is `POST /distance-matrix` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-distance-matrix.md) for the provider-specific parameters and requirements.

