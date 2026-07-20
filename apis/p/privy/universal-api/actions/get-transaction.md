# Privy: Get Transaction

Retrieves a transaction from Privy by ID.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction?${params}`, {
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
| `transactionId` | string | yes | Privy transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caip2": "string",
      "created_at": 1,
      "id": "string",
      "reference_id": "string",
      "sponsored": true,
      "status": "string",
      "transaction_hash": "string",
      "wallet_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caip2` | string |  |
| `created_at` | number |  |
| `id` | string |  |
| `reference_id` | string |  |
| `sponsored` | boolean |  |
| `status` | string |  |
| `transaction_hash` | string |  |
| `wallet_id` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/transactions/{{transactionId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

