# Precisely: Timezone By Address

Retrieves time zone details from Precisely by address.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-address?connectionId=$CONNECTION_ID&address=string&timestamp=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "timestamp": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/timezone-by-address?${params}`, {
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
| `address` | string | yes | Single-line address to resolve to a timezone. |
| `timestamp` | number | yes | Unix timestamp in milliseconds for the moment to evaluate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dstOffset": 1,
      "matchedAddress": {
        "addressLastLine": "string",
        "areaName1": "Ava Chen",
        "areaName2": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "formattedAddress": "string"
      },
      "timestamp": 1,
      "timezoneName": "Ava Chen",
      "utcOffset": 1,
      "zoneType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dstOffset` | number | Daylight saving offset in milliseconds. |
| `matchedAddress.addressLastLine` | string | City, county, region, and country line. |
| `matchedAddress.areaName1` | string | Top-level administrative area, typically state or province. |
| `matchedAddress.areaName2` | string | Secondary administrative area, typically county or district. |
| `matchedAddress.areaName3` | string | City or locality name. |
| `matchedAddress.country` | string | Country code or country name. |
| `matchedAddress.formattedAddress` | string | Formatted matched address. |
| `timestamp` | number | Evaluated Unix timestamp in milliseconds. |
| `timezoneName` | string | Human-readable timezone name. |
| `utcOffset` | number | UTC offset in milliseconds. |
| `zoneType` | string | IANA timezone identifier. |

## Native endpoint

Through the native Precisely API, this operation is `GET /timezone/v1/timezone/byaddress` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/timezone-by-address.md) for the provider-specific parameters and requirements.

