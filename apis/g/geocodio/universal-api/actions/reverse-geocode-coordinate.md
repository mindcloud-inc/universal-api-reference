# Geocodio: Reverse Geocode Coordinate

Retrieves address details from Geocodio for one coordinate.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/reverse-geocode-coordinate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/reverse-geocode-coordinate?connectionId=$CONNECTION_ID&q=38.886672%2C-77.094735" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "38.886672,-77.094735"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/reverse-geocode-coordinate?${params}`, {
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
| `q` | string | yes | Latitude and longitude to reverse geocode, formatted as lat,lng. Example: `38.886672,-77.094735`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional comma-separated list of data append fields. Accepts multiple values in one string, delimited by `,`. Example: `timezone`. |
| `skipGeocoding` | boolean | no | When present, extracts field data from coordinates without reverse geocoding. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "accuracy": 1,
          "accuracyType": "string",
          "formattedAddress": "string",
          "location": {
            "lat": 1,
            "lng": 1
          },
          "stableAddressKey": "string"
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
| `results` | array<object> | Reverse geocoding results ordered by proximity/accuracy. |
| `results[].accuracy` | number | Geocodio accuracy score. |
| `results[].accuracyType` | string | Accuracy type reported by Geocodio. |
| `results[].formattedAddress` | string | Formatted address for the matched coordinate. |
| `results[].location.lat` | number | Latitude of the matched address. |
| `results[].location.lng` | number | Longitude of the matched address. |
| `results[].stableAddressKey` | string | Stable address key for the result. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /reverse` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-coordinate.md) for the provider-specific parameters and requirements.

