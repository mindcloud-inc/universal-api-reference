# OneMap SG: Reverse Geocode (Latitude and Longitude)

Retrieves an address from OneMap SG by latitude and longitude.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-lat-lng
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-lat-lng?connectionId=$CONNECTION_ID&location=1.3254295%2C103.9005321" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "1.3254295,103.9005321"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-lat-lng?${params}`, {
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
| `location` | string | yes | Latitude and longitude as a comma-separated pair. Example: `1.3254295,103.9005321`. |
| `buffer` | number | no | The search buffer around the location. Default: `40`. Example: `40`. |
| `addressType` | string | no | The address type to include in the reverse geocode response. Default: `All`. Example: `All`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "GeocodeInfo": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `GeocodeInfo` | array<object> | The reverse geocode matches for the supplied latitude and longitude. |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/revgeocode` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-lat-lng.md) for the provider-specific parameters and requirements.

