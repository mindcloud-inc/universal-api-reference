# Visma eAccounting: Get Customer Invoice

Retrieves a customer invoice from Visma eAccounting.

```
GET https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/get-customer-invoice?${params}`, {
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

Through the native Visma eAccounting API, this operation is `GET /customerinvoices/{invoiceId}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-invoice.md) for the provider-specific parameters and requirements.

