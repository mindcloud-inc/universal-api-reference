# Geocodio: Batch Geocode Addresses

Retrieves geocoding results from Geocodio for multiple addresses.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-geocode-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-geocode-addresses?connectionId=$CONNECTION_ID&payload%5B%5D=1109%20N%20Highland%20St%2C%20Arlington%20VA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payload[]": "1109 N Highland St, Arlington VA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/batch-geocode-addresses?${params}`, {
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
| `payload[]` | array<string> | yes | Array or keyed object of addresses to geocode. Example: `1109 N Highland St, Arlington VA`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional comma-separated list of data append fields. Accepts multiple values in one string, delimited by `,`. Example: `timezone,cd`. |
| `limit` | number | no | Optional maximum number of results per address. Example: `1`. |

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
| `results` | array<object> | Batch geocoding results. |
| `results[].query` | string | Input address query. |
| `results[].response` | object | Geocoding response for the input query. |
| `results[].response.results` | array<object> | Candidate geocoding results for the query. |
| `results[].response.results[].formattedAddress` | string | Formatted address for a candidate result. |
| `results[].response.results[].location.lat` | number | Latitude for a candidate result. |
| `results[].response.results[].location.lng` | number | Longitude for a candidate result. |

## Native endpoint

Through the native Geocodio API, this operation is `POST /geocode` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-geocode-addresses.md) for the provider-specific parameters and requirements.

