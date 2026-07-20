# Merit: Create Sales Invoice



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Customer": {},
  "DocDate": "string",
  "DueDate": "string",
  "InvoiceNo": "string",
  "InvoiceRow[]": [
    {}
  ],
  "TaxAmount[]": [
    {}
  ],
  "TotalAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-sales-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Customer": {},
    "DocDate": "string",
    "DueDate": "string",
    "InvoiceNo": "string",
    "InvoiceRow[]": [{}],
    "TaxAmount[]": [{}],
    "TotalAmount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Customer` | object | yes | Customer object, for example {"Id":"..."}. |
| `DocDate` | string | yes | Invoice date in Merit date string format. |
| `DueDate` | string | yes | Invoice due date in Merit date string format. |
| `InvoiceNo` | string | yes | Invoice number. |
| `InvoiceRow[]` | array<object> | yes | Array of invoice row objects. |
| `TaxAmount[]` | array<object> | yes | Array of tax amount objects. |
| `TotalAmount` | number | yes | Invoice total amount. |
| `CurrencyCode` | string | no | Currency code, for example EUR. Default: `EUR`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerId": "string",
      "InvoiceId": "string",
      "InvoiceNo": "string",
      "NewCustomer": "string",
      "RefNo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerId` | string | Customer identifier linked to the created invoice. |
| `InvoiceId` | string | Created invoice identifier. |
| `InvoiceNo` | string | Created invoice number. |
| `NewCustomer` | string | New customer identifier when Merit created a customer inline. |
| `RefNo` | string | Reference number when present. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendinvoice` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-invoice.md) for the provider-specific parameters and requirements.

