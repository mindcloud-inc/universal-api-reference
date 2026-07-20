# Bexio: Get Expense

Retrieves an expense from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-expense?connectionId=$CONNECTION_ID&expenseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expenseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-expense?${params}`, {
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
| `expenseId` | string | yes | The expense UUID. |

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

Through the native Bexio API, this operation is `GET /4.0/expenses/:id` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

