# Escrow.com: Get Transaction

Retrieves a transaction from Escrow.com.

```
GET https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/get-transaction?${params}`, {
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
| `transactionId` | number | yes | The Escrow.com transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closeDate": "2026-05-07T12:00:00.000Z",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": 1,
      "items": [
        {}
      ],
      "parties": [
        {}
      ],
      "partnerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closeDate` | date | Transaction close timestamp when available. |
| `creationDate` | date | Transaction creation timestamp. |
| `currency` | string | Transaction currency code. |
| `description` | string | Transaction description. |
| `id` | number | Escrow.com transaction ID. |
| `items` | array<object> | Milestone or general merchandise items in the transaction. |
| `parties` | array<object> | Buyer, seller, broker, and partner parties on the transaction. |
| `partnerId` | number | Partner identifier associated with the transaction when available. |

## Native endpoint

Through the native Escrow.com API, this operation is `GET /transaction/:transaction_id` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

