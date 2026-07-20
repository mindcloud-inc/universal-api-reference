# Addressfinder: Verify AU Address

Verifies a full Australian address in Addressfinder.

```
GET https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/verify-au-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Addressfinder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/verify-au-address?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/verify-au-address?${params}`, {
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
| `q` | string | yes | The address to be verified. |
| `gnaf` | string | no | Set to 1 to query the GNAF database. Default: `1`. |
| `paf` | string | no | Set to 1 to query the PAF database. Default: `1`. |
| `gps` | string | no | Set to 1 to return latitude and longitude when available. |
| `extended` | string | no | Set to 1 to return additional GNAF metadata. |
| `census` | number | no | Census year used for statistical area identifiers. |
| `stateCodes` | string | no | Filter results by state or territory codes. |
| `domain` | string | no | Registered domain used for activity monitoring. |
| `postBox` | string | no | Set to 0 to exclude box-type addresses from verification results. |
| `ascii` | string | no | Set to 1 to normalize special characters to ASCII equivalents. |
| `format` | string | no | Response format. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Addressfinder API returns.

## Native endpoint

Through the native Addressfinder API, this operation is `GET /au/address/v2/verification` (base URL `https://api.addressfinder.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-au-address.md) for the provider-specific parameters and requirements.

