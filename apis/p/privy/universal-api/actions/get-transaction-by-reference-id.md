# Privy: Get Transaction By Reference ID

Finds transactions in Privy by reference ID.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction-by-reference-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction-by-reference-id?connectionId=$CONNECTION_ID&referenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "referenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-transaction-by-reference-id?${params}`, {
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
| `referenceId` | string | yes | External reference ID for transaction lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transactions": [
        {
          "created_at": 1,
          "id": "string",
          "reference_id": "string",
          "status": "string",
          "transaction_hash": "string",
          "wallet_id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transactions[].created_at` | number |  |
| `transactions[].id` | string |  |
| `transactions[].reference_id` | string |  |
| `transactions[].status` | string |  |
| `transactions[].transaction_hash` | string |  |
| `transactions[].wallet_id` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/transactions` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-by-reference-id.md) for the provider-specific parameters and requirements.

