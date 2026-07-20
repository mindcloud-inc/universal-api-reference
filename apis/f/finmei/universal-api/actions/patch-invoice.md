# Finmei: Patch Invoice



```
PUT https://connect.mindcloud.co/v1/universal/finmei/latest/actions/patch-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/patch-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmei/latest/actions/patch-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buyer` | object | no | Buyer object. |
| `buyer.country` | string | no | Buyer country code. |
| `buyer.first_name` | string | no | Buyer first name. |
| `buyer.last_name` | string | no | Buyer last name. |
| `buyer.type` | string | no | Buyer type. |
| `currency` | string | no | Invoice currency code. |
| `invoice_date` | date | no | Invoice issue date. |
| `invoiceId` | string | yes |  |
| `products` | list<object> | no | Invoice line items. |
| `products[].name` | string | no | Product or service name. |
| `products[].price` | number | no | Product unit price. |
| `products[].quantity` | number | no | Product quantity. |
| `products[].units` | string | no | Units label. |
| `products[].vat_percentage` | number | no | VAT percentage for VAT invoice variants. |
| `series` | string | no | Invoice series identifier. |
| `type` | string | no | Invoice type enum observed from Finmei. |
| `use_default_seller_info` | boolean | no | Whether to use the default seller information. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "businessId": "string",
        "buyer": {
          "firstName": "Ava",
          "lastName": "Chen",
          "type": "string"
        },
        "createdAt": 1,
        "currency": "string",
        "id": "string",
        "invoiceDate": "string",
        "invoiceNumber": "string",
        "invoiceType": "string",
        "items": [
          {
            "name": "Ava Chen",
            "price": 1,
            "quantity": 1,
            "units": "string",
            "vatPercentage": 1
          }
        ],
        "paymentStatus": "string",
        "shareLink": "https://example.com",
        "totalInclVat": 1,
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.businessId` | string |  |
| `data.buyer.firstName` | string |  |
| `data.buyer.lastName` | string |  |
| `data.buyer.type` | string |  |
| `data.createdAt` | number |  |
| `data.currency` | string |  |
| `data.id` | string |  |
| `data.invoiceDate` | string |  |
| `data.invoiceNumber` | string |  |
| `data.invoiceType` | string |  |
| `data.items` | array<object> |  |
| `data.items[].name` | string |  |
| `data.items[].price` | number |  |
| `data.items[].quantity` | number |  |
| `data.items[].units` | string |  |
| `data.items[].vatPercentage` | number |  |
| `data.paymentStatus` | string |  |
| `data.shareLink` | string |  |
| `data.totalInclVat` | number |  |
| `data.updatedAt` | number |  |

## Native endpoint

Through the native Finmei API, this operation is `PATCH /invoices/:invoiceId` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-invoice.md) for the provider-specific parameters and requirements.

