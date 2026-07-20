# Addressfinder: List AU Address Suggestions

Finds Australian address suggestions in Addressfinder by partial query.

```
GET https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Addressfinder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/list-au-address-suggestions?${params}`, {
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
| `q` | string | no | The partial address being searched. |
| `source` | string | no | Address source dataset filter. Default: `GNAF,PAF`. |
| `stateCodes` | string | no | Filter results by state or territory codes. |
| `max` | number | no | Maximum number of suggestions to return. Default: `10`. |
| `format` | string | no | Response format. Default: `json`. |
| `domain` | string | no | Registered domain used for activity monitoring. |
| `postBox` | string | no | Include or restrict PO Box style addresses. |
| `canonical` | string | no | Exclude alias addresses when set. |
| `highlight` | string | no | Highlight matching terms in the returned address text. |
| `ascii` | string | no | Normalize special characters to ASCII equivalents. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Addressfinder API returns.

## Native endpoint

Through the native Addressfinder API, this operation is `GET /au/address/autocomplete` (base URL `https://api.addressfinder.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-au-address-suggestions.md) for the provider-specific parameters and requirements.

