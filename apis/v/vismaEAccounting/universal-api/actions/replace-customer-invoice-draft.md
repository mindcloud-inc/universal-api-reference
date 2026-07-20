# Visma eAccounting: Replace Customer Invoice Draft

Updates an existing customer invoice draft in Visma eAccounting.

```
PUT https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/replace-customer-invoice-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/replace-customer-invoice-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/replace-customer-invoice-draft', {
  method: 'PUT',
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
      "customerId": "string",
      "customerName": "Ava Chen",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceDate": "2026-05-07T12:00:00.000Z",
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
| `customerId` | string |  |
| `customerName` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `invoiceDate` | date |  |
| `rows[]` | array<object> |  |
| `rows[].id` | string |  |
| `rows[].quantity` | number |  |
| `rows[].text` | string |  |
| `rows[].unitPrice` | number |  |
| `totalAmount` | number |  |
| `totalVatAmount` | number |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `PUT /customerinvoicedrafts/{customerInvoiceDraftId}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-customer-invoice-draft.md) for the provider-specific parameters and requirements.

