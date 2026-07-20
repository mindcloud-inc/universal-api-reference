# MoneyBird: Create Sales Invoice

Creates a new sales invoice in MoneyBird.

```
POST https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-sales-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-sales-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "administrationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-sales-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "administrationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `administrationId` | string | yes | Moneybird administration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "contact": {},
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "details": [
        {}
      ],
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceId": "string",
      "paidAt": "2026-05-07T12:00:00.000Z",
      "payments": [
        {}
      ],
      "reference": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "totalPriceExclTax": "string",
      "totalPriceInclTax": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `contact` | object |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `details` | array<object> |  |
| `dueDate` | date |  |
| `id` | string |  |
| `invoiceDate` | date |  |
| `invoiceId` | string |  |
| `paidAt` | date |  |
| `payments` | array<object> |  |
| `reference` | string |  |
| `sentAt` | date |  |
| `state` | string |  |
| `totalPriceExclTax` | string |  |
| `totalPriceInclTax` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native MoneyBird API, this operation is `POST /:administrationId/sales_invoices.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-invoice.md) for the provider-specific parameters and requirements.

