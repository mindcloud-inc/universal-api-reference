# Becon: List Stores

Retrieves created store records from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-stores?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "binance_address": "string",
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "tag": "string",
      "xpub": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binance_address` | string | Binance chain address when available. |
| `created_at` | string | Store creation timestamp. |
| `id` | number | Store identifier. |
| `name` | string | Store name. |
| `tag` | string | Store tag. |
| `xpub` | string | Extended public key for Bitcoin stores when available. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/stores` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores.md) for the provider-specific parameters and requirements.

