# Soundee: List Transactions

Retrieves your transaction records from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/list-transactions?${params}`, {
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
| `listType` | string | no | Filter transactions by type. |
| `search` | string | no | Search by item, customer, collaborator, amount, email, or transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressDetails": {},
      "created": 1,
      "currency": {},
      "customer": {},
      "fee": "string",
      "gross": 1,
      "id": 1,
      "invoice": {},
      "ip": "string",
      "items": [
        {}
      ],
      "merchant": {},
      "net": 1,
      "parameters": {},
      "parentTransactionId": "string",
      "paymentSource": {},
      "paymentStatus": "string",
      "receiptUrl": "https://example.com",
      "store": {},
      "tax": 1,
      "taxRate": 1,
      "transactionId": "string",
      "transactionType": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressDetails` | object |  |
| `created` | number |  |
| `currency` | object |  |
| `customer` | object |  |
| `fee` | string |  |
| `gross` | number |  |
| `id` | number |  |
| `invoice` | object |  |
| `ip` | string |  |
| `items` | array<object> |  |
| `merchant` | object |  |
| `net` | number |  |
| `parameters` | object |  |
| `parentTransactionId` | string |  |
| `paymentSource` | object |  |
| `paymentStatus` | string |  |
| `receiptUrl` | string |  |
| `store` | object |  |
| `tax` | number |  |
| `taxRate` | number |  |
| `transactionId` | string |  |
| `transactionType` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Soundee API, this operation is `GET /transactions` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

