# Addressfinder: Get AU Address Metadata

Retrieves metadata for an Australian address from Addressfinder.

```
GET https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-address-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Addressfinder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-address-metadata?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-address-metadata?${params}`, {
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
| `id` | string | yes | Unique address identifier obtained from the AU Address Autocomplete API. |
| `source` | string | no | Address source dataset filter. Default: `GNAF,PAF`. |
| `gps` | string | no | Set to 1 to include latitude and longitude when available. |
| `census` | number | no | Census year used for statistical area identifiers. Default: `2016`. |
| `domain` | string | no | Registered domain used for activity monitoring. |
| `ascii` | string | no | Set to 1 to normalize special characters to ASCII equivalents. |
| `format` | string | no | Response format. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Addressfinder API returns.

## Native endpoint

Through the native Addressfinder API, this operation is `GET /au/address/metadata` (base URL `https://api.addressfinder.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-au-address-metadata.md) for the provider-specific parameters and requirements.

