# Digistore24: List Transactions

Retrieves payments, returns, and chargebacks from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-transactions?${params}`, {
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
| `from` | string | no | Start date/time |
| `to` | string | no | End date/time |
| `search` | object | no | Structured search filters |
| `search.role` | string | no | Filter by role |
| `search.productId` | string | no | Filter by product ID |
| `search.firstName` | string | no | Filter by buyer first name |
| `search.lastName` | string | no | Filter by buyer last name |
| `search.email` | string | no | Filter by buyer email |
| `search.hasAffiliate` | boolean | no | Filter transactions with or without affiliate |
| `search.affiliateName` | string | no | Filter by affiliate name |
| `search.payMethod` | string | no | Filter by payment method |
| `search.billingType` | string | no | Filter by billing type |
| `search.transactionType` | string | no | Filter by transaction type |
| `search.currency` | string | no | Filter by currency code |
| `search.purchaseId` | string | no | Filter by purchase ID |
| `sortBy` | string | no | Sort transactions |
| `sortOrder` | string | no | Sort order |
| `pageNo` | number | no | Page number |
| `pageSize` | number | no | Page size |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "buyer": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "id": 1,
      "purchaseId": "string",
      "transactionType": "string",
      "transactionTypeMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount |
| `buyer.email` | string | Buyer email |
| `buyer.firstName` | string | Buyer first name |
| `buyer.id` | number | Buyer ID |
| `buyer.lastName` | string | Buyer last name |
| `createdAt` | date | Creation timestamp |
| `currency` | string | Currency code |
| `id` | number | Transaction ID |
| `purchaseId` | string | Purchase ID |
| `transactionType` | string | Transaction type |
| `transactionTypeMsg` | string | Transaction type label |

## Native endpoint

Through the native Digistore24 API, this operation is `POST /listTransactions` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

