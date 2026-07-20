# InstantCard: List Financial Transactions

Retrieves all financial transactions from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-financial-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-financial-transactions?connectionId=$CONNECTION_ID&organizationId=20003827" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-financial-transactions?${params}`, {
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
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "created_at": "string",
      "credit": "string",
      "debit": "string",
      "description": "string",
      "id": 1,
      "receipt": true,
      "sub_type": "string",
      "transaction_items": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string | Balance after the transaction. |
| `created_at` | string | Transaction creation timestamp. |
| `credit` | string | Credit amount. |
| `debit` | string | Debit amount. |
| `description` | string | Transaction description. |
| `id` | number | Transaction ID. |
| `receipt` | boolean | Whether a receipt is available. |
| `sub_type` | string | Transaction subtype. |
| `transaction_items` | object | Expanded transaction detail payload. |
| `type` | string | Transaction type. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/financial_transactions` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-financial-transactions.md) for the provider-specific parameters and requirements.

