# Strale: List Transactions

Retrieves transactions from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-transactions?${params}`, {
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
      "capabilitySlug": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "latencyMs": 1,
      "priceCents": 1,
      "solutionSlug": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilitySlug` | string | Capability slug when the transaction is capability-based. |
| `completedAt` | date | Transaction completion timestamp. |
| `createdAt` | date | Transaction creation timestamp. |
| `id` | string | Transaction identifier. |
| `latencyMs` | number | Observed latency in milliseconds. |
| `priceCents` | number | Transaction price in cents. |
| `solutionSlug` | string | Solution slug when the transaction is solution-based. |
| `status` | string | Transaction status. |
| `type` | string | Transaction type. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/transactions` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

