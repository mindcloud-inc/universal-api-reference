# Mempool: Get Address Summary

Retrieves summary details for an address from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-address-summary?${params}`, {
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
| `address` | string | yes | Bitcoin address to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "chain_stats": {},
      "mempool_stats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `chain_stats` | object |  |
| `mempool_stats` | object |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /address/[:address]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-summary.md) for the provider-specific parameters and requirements.

