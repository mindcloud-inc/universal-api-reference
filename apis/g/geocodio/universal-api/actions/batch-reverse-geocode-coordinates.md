# Geocodio: Batch Reverse Geocode Coordinates

Retrieves address details from Geocodio for multiple coordinates.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-reverse-geocode-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-reverse-geocode-coordinates?connectionId=$CONNECTION_ID&payload%5B%5D=38.886672%2C-77.094735" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payload[]": "38.886672,-77.094735"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-reverse-geocode-coordinates?${params}`, {
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
| `payload[]` | array<string> | yes | Array or keyed object of coordinates to reverse geocode. Example: `38.886672,-77.094735`. |

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
          "query": "string",
          "response": {
            "results": [
              {
                "formattedAddress": "string",
                "location": {
                  "lat": 1,
                  "lng": 1
                }
              }
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
| `results` | array<object> | Batch reverse geocoding results. |
| `results[].query` | string | Input coordinate query. |
| `results[].response` | object | Reverse geocoding response for the input coordinate. |
| `results[].response.results` | array<object> | Candidate address results for the coordinate. |
| `results[].response.results[].formattedAddress` | string | Formatted address for a candidate result. |
| `results[].response.results[].location.lat` | number | Latitude for a candidate result. |
| `results[].response.results[].location.lng` | number | Longitude for a candidate result. |

## Native endpoint

Through the native Geocodio API, this operation is `POST /reverse` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-reverse-geocode-coordinates.md) for the provider-specific parameters and requirements.

