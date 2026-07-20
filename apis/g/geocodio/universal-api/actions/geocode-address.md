# Geocodio: Geocode Address

Retrieves geocoding results from Geocodio for one address.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address?connectionId=$CONNECTION_ID&q=1109%20N%20Highland%20St%2C%20Arlington%20VA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "1109 N Highland St, Arlington VA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address?${params}`, {
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
| `q` | string | yes | The address, city, ZIP/postal code, or stable address key to geocode. Example: `1109 N Highland St, Arlington VA`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Optional country to geocode in. Supported values are USA, Canada, or Mexico. Example: `USA`. |
| `fields` | string | no | Optional comma-separated list of data append fields, such as timezone, cd, census, zip4, or acs-demographics. Accepts multiple values in one string, delimited by `,`. Example: `timezone,cd`. |
| `limit` | number | no | Optional maximum number of geocoding results to return. Example: `5`. |
| `format` | string | no | Optional response format. Geocodio currently documents simple as the alternate format. One of: `0`. Example: `simple`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {
        "addressComponents": {},
        "formattedAddress": "string"
      },
      "results": [
        {
          "accuracy": 1,
          "accuracyType": "string",
          "formattedAddress": "string",
          "location": {
            "lat": 1,
            "lng": 1
          },
          "matchType": "string",
          "source": "string",
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
| `input` | object | Parsed input address returned by Geocodio. |
| `input.addressComponents` | object | Parsed input address components. |
| `input.formattedAddress` | string | Formatted input address. |
| `results` | array<object> | Candidate geocoding results ordered by accuracy. |
| `results[].accuracy` | number | Geocodio accuracy score. |
| `results[].accuracyType` | string | Accuracy type reported by Geocodio. |
| `results[].formattedAddress` | string | Formatted address for the geocoded result. |
| `results[].location` | object | Latitude and longitude for the result. |
| `results[].location.lat` | number | Latitude for the result. |
| `results[].location.lng` | number | Longitude for the result. |
| `results[].matchType` | string | Match type reported by Geocodio. |
| `results[].source` | string | Source dataset for the result. |
| `results[].stableAddressKey` | string | Stable address key for the result. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /geocode` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-address.md) for the provider-specific parameters and requirements.

