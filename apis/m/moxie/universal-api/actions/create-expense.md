# Moxie: Create Expense

Creates a new expense in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-05-07T12:00:00.000Z",
  "amount": 1,
  "currency": "string",
  "paid": true,
  "reimbursable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-05-07T12:00:00.000Z",
    "amount": 1,
    "currency": "string",
    "paid": true,
    "reimbursable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billNo` | string | no | Optional bill number for the expense. |
| `category` | string | no | Optional expense category name. |
| `date` | date | yes | Expense date. |
| `markupPercentage` | number | no | Optional markup percentage to apply when the expense is reimbursable. Defaults to 0 to avoid Moxie sample-mode response errors. Default: `0`. |
| `notes` | string | no | Optional notes for the expense. |
| `amount` | number | yes | Expense amount. |
| `currency` | string | yes | Expense currency code. |
| `paid` | boolean | yes | Whether the expense has been paid. |
| `reimbursable` | boolean | yes | Whether the expense is reimbursable. |
| `vendor` | string | no | Vendor name for the expense. |
| `clientName` | string | no | Client name tied to the expense. |
| `description` | string | no | Expense description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amount": 1,
      "attachments": [
        {}
      ],
      "client": {},
      "clientId": "string",
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "integrationKeys": {},
      "markupPercent": 1,
      "paid": true,
      "paidDate": "2026-05-07T12:00:00.000Z",
      "reimbursable": true,
      "sampleData": true,
      "total": 1,
      "totalWithMarkup": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amount` | number |  |
| `attachments` | array<object> |  |
| `client` | object |  |
| `clientId` | string |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `description` | string |  |
| `id` | string |  |
| `integrationKeys` | object |  |
| `markupPercent` | number |  |
| `paid` | boolean |  |
| `paidDate` | date |  |
| `reimbursable` | boolean |  |
| `sampleData` | boolean |  |
| `total` | number |  |
| `totalWithMarkup` | number |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/expenses/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

