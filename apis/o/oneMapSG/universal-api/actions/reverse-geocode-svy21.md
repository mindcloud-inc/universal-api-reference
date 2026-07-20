# OneMap SG: Reverse Geocode (SVY21 Coordinates)

Retrieves an address from OneMap SG by SVY21 coordinates.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-svy21
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-svy21?connectionId=$CONNECTION_ID&location=24291.97788882387%2C31373.0117224489" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "24291.97788882387,31373.0117224489"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/reverse-geocode-svy21?${params}`, {
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
| `location` | string | yes | SVY21 X and Y coordinates as a comma-separated pair. Example: `24291.97788882387,31373.0117224489`. |
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
| `GeocodeInfo` | array<object> |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/public/revgeocodexy` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-svy21.md) for the provider-specific parameters and requirements.

