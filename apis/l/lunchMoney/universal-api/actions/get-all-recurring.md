# Lunch Money: Get all recurring items



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-recurring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-recurring?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-all-recurring?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "id": 1,
      "matches": {
        "expectedOccurrenceDates": [
          "2026-05-07T12:00:00.000Z"
        ],
        "foundTransactions": {
          "date": "2026-05-07T12:00:00.000Z",
          "transactionId": "string"
        },
        "missingTransactionDates": [
          "2026-05-07T12:00:00.000Z"
        ],
        "requestEndDate": "2026-05-07T12:00:00.000Z",
        "requestStartDate": "2026-05-07T12:00:00.000Z"
      },
      "overrides": {
        "categoryId": "string",
        "notes": "string",
        "payee": "string"
      },
      "source": "string",
      "status": "string",
      "transactionCriteria": {
        "amount": "string",
        "anchorDate": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "endDate": "2026-05-07T12:00:00.000Z",
        "granularity": "string",
        "manualAccountId": 1,
        "payee": "string",
        "plaidAccountId": 1,
        "quantity": "string",
        "startDate": "2026-05-07T12:00:00.000Z",
        "toBase": 1
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `description` | string |  |
| `id` | number |  |
| `matches` | object |  |
| `matches.expectedOccurrenceDates` | array<date> |  |
| `matches.foundTransactions` | array<object> |  |
| `matches.foundTransactions.date` | date |  |
| `matches.foundTransactions.transactionId` | string |  |
| `matches.missingTransactionDates` | array<date> |  |
| `matches.requestEndDate` | date |  |
| `matches.requestStartDate` | date |  |
| `overrides` | object |  |
| `overrides.categoryId` | string |  |
| `overrides.notes` | string |  |
| `overrides.payee` | string |  |
| `source` | string |  |
| `status` | string |  |
| `transactionCriteria` | object |  |
| `transactionCriteria.amount` | string |  |
| `transactionCriteria.anchorDate` | date |  |
| `transactionCriteria.currency` | string |  |
| `transactionCriteria.endDate` | date |  |
| `transactionCriteria.granularity` | string |  |
| `transactionCriteria.manualAccountId` | number |  |
| `transactionCriteria.payee` | string |  |
| `transactionCriteria.plaidAccountId` | number |  |
| `transactionCriteria.quantity` | string |  |
| `transactionCriteria.startDate` | date |  |
| `transactionCriteria.toBase` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /recurring_items` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-recurring.md) for the provider-specific parameters and requirements.

