# Bexio: Create Expense

Creates an expense in Bexio.

```
POST https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paidOn": "2026-05-07T12:00:00.000Z",
  "currencyCode": "string",
  "amount": 1,
  "attachmentIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paidOn": "2026-05-07T12:00:00.000Z",
    "currencyCode": "string",
    "amount": 1,
    "attachmentIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paidOn` | date | yes | Date when the expense was paid. |
| `currencyCode` | string | yes |  |
| `supplierId` | number | no |  |
| `title` | string | no |  |
| `bankAccountId` | number | no |  |
| `bookingAccountId` | number | no |  |
| `amount` | number | yes |  |
| `taxId` | number | no |  |
| `exchangeRate` | number | no |  |
| `baseCurrencyAmount` | number | no |  |
| `attachmentIds[]` | array<string> | yes |  |
| `address` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "amount": 1,
      "averageExchangeRateEnabled": true,
      "bankAccountId": {},
      "baseCurrencyAmount": 1,
      "baseCurrencyCode": "string",
      "bookingAccountId": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "documentNo": "string",
      "exchangeRate": 1,
      "firstnameSuffix": {},
      "id": "string",
      "invoiceId": {},
      "lastnameCompany": "Chen",
      "paidOn": "2026-05-07T12:00:00.000Z",
      "projectId": {},
      "status": "string",
      "supplierId": 1,
      "taxCalc": 1,
      "taxId": {},
      "taxMan": 1,
      "title": "string",
      "transactionId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `amount` | number |  |
| `averageExchangeRateEnabled` | boolean |  |
| `bankAccountId` | object |  |
| `baseCurrencyAmount` | number |  |
| `baseCurrencyCode` | string |  |
| `bookingAccountId` | object |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `documentNo` | string |  |
| `exchangeRate` | number |  |
| `firstnameSuffix` | object |  |
| `id` | string |  |
| `invoiceId` | object |  |
| `lastnameCompany` | string |  |
| `paidOn` | date |  |
| `projectId` | object |  |
| `status` | string |  |
| `supplierId` | number |  |
| `taxCalc` | number |  |
| `taxId` | object |  |
| `taxMan` | number |  |
| `title` | string |  |
| `transactionId` | object |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /4.0/expenses` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

