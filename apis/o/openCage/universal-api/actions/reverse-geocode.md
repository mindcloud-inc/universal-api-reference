# OpenCage: Reverse Geocode

Retrieves location details from OpenCage by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/openCage/latest/actions/reverse-geocode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenCage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openCage/latest/actions/reverse-geocode?connectionId=$CONNECTION_ID&q=52.5432379%2C13.4142133" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "52.5432379,13.4142133"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openCage/latest/actions/reverse-geocode?${params}`, {
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
| `q` | string | yes | Latitude and longitude in decimal format, in latitude,longitude order. Example: `52.5432379,13.4142133`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Optional language code to favor in returned results, such as `de`, `pt-BR`, or `native`. Example: `en`. |
| `addressOnly` | string | no | Optional flag. Set to `1` to include only the address in the formatted string when possible. Example: `1`. |
| `roadinfo` | string | no | Optional flag. Set to `1` to match the nearest road and include road information when possible. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentation": "https://example.com",
      "licenses": [
        {}
      ],
      "rate": {},
      "results": [
        {}
      ],
      "status": {},
      "thanks": "string",
      "timestamp": {},
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentation` | string | OpenCage API documentation URL returned with the response. |
| `licenses` | array<object> | Attribution and license metadata for returned geocoding data. |
| `rate` | object | Rate-limit details returned for accounts with hard limits. |
| `results` | array<object> | Reverse geocoding result object array. Reverse requests return at most one result and may include distance_from_q. |
| `status` | object | Response status code and message. |
| `thanks` | string | OpenCage thank-you message. |
| `timestamp` | object | Response creation timestamp. |
| `total_results` | number | Total number of reverse geocoding results. |

## Native endpoint

Through the native OpenCage API, this operation is `GET /json` (base URL `https://api.opencagedata.com/geocode/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode.md) for the provider-specific parameters and requirements.

