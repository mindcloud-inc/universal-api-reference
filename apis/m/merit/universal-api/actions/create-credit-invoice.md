# Merit: Create Credit Invoice



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-credit-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-credit-invoice" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-credit-invoice', {
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
| `InvoiceNo` | string | yes | Credit invoice number. |
| `InvoiceRow[]` | array<object> | yes | Array of invoice row objects with negative quantities for crediting. |
| `TaxAmount[]` | array<object> | yes | Array of tax amount objects. |
| `TotalAmount` | number | yes | Credit invoice total amount. |
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
| `CustomerId` | string | Customer identifier linked to the created credit invoice. |
| `InvoiceId` | string | Created credit invoice identifier. |
| `InvoiceNo` | string | Created credit invoice number. |
| `NewCustomer` | string | New customer identifier when Merit created a customer inline. |
| `RefNo` | string | Reference number when present. |

## Native endpoint

Through the native Merit API, this operation is `POST v1/sendinvoice` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-credit-invoice.md) for the provider-specific parameters and requirements.

