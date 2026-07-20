# Skyfire: Get Agent Wallet Balance

Retrieves an agent wallet balance from Skyfire.

```
GET https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-wallet-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/get-agent-wallet-balance?${params}`, {
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
      "available": "string",
      "heldAmount": "string",
      "pendingCharges": "string",
      "pendingDeposits": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | string |  |
| `heldAmount` | string |  |
| `pendingCharges` | string |  |
| `pendingDeposits` | string |  |

## Native endpoint

Through the native Skyfire API, this operation is `GET /agents/balance` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-wallet-balance.md) for the provider-specific parameters and requirements.

