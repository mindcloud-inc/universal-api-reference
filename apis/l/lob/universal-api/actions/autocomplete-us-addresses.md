# Lob: Autocomplete US Addresses



```
GET https://connect.mindcloud.co/v1/universal/lob/latest/actions/autocomplete-us-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lob/latest/actions/autocomplete-us-addresses?connectionId=$CONNECTION_ID&addressPrefix=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "addressPrefix": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lob/latest/actions/autocomplete-us-addresses?${params}`, {
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
| `addressPrefix` | string | yes | Partial primary line to autocomplete. |
| `city` | string | no | Optional city filter. |
| `state` | string | no | Optional state filter. |
| `zipCode` | string | no | Optional ZIP code filter. |
| `geoIpSort` | boolean | no | Sort suggestions by client IP proximity when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "suggestions": [
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
| `id` | string |  |
| `object` | string |  |
| `suggestions` | array<object> |  |

## Native endpoint

Through the native Lob API, this operation is `POST /us_autocompletions` (base URL `https://api.lob.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-us-addresses.md) for the provider-specific parameters and requirements.

