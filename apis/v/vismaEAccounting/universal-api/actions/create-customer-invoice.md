# Visma eAccounting: Create Customer Invoice

Creates a new customer invoice in Visma eAccounting.

```
POST https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/create-customer-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyCode": "string",
      "customerId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceNumber": "string",
      "isCreditInvoice": true,
      "rows": [
        [
          {}
        ]
      ],
      "totalAmount": 1,
      "totalVatAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `invoiceDate` | date |  |
| `invoiceNumber` | string |  |
| `isCreditInvoice` | boolean |  |
| `rows[]` | array<object> |  |
| `rows[].id` | string |  |
| `rows[].quantity` | number |  |
| `rows[].text` | string |  |
| `rows[].unitPrice` | number |  |
| `totalAmount` | number |  |
| `totalVatAmount` | number |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `POST /customerinvoices` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-invoice.md) for the provider-specific parameters and requirements.

