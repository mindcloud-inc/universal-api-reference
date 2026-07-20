# Privy: List Wallet Transactions

Retrieves transactions for a wallet from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallet-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallet-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0&walletId=string&chain=string&asset=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "walletId": "string",
  "chain": "string",
  "asset": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-wallet-transactions?${params}`, {
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
| `walletId` | string | yes | Privy wallet ID. |
| `chain` | string | yes | Blockchain/network to fetch transactions for. |
| `asset` | string | yes | Asset to fetch transactions for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `txHash` | string | no | Optional transaction hash filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_cursor": "string",
      "transactions": [
        {
          "caip2": "string",
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
| `next_cursor` | string |  |
| `transactions[].caip2` | string |  |
| `transactions[].created_at` | number |  |
| `transactions[].id` | string |  |
| `transactions[].reference_id` | string |  |
| `transactions[].status` | string |  |
| `transactions[].transaction_hash` | string |  |
| `transactions[].wallet_id` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/wallets/{{walletId}}/transactions` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wallet-transactions.md) for the provider-specific parameters and requirements.

