# Finmei: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buyer": {},
  "buyer.country": "string",
  "buyer.first_name": "Ava",
  "buyer.last_name": "Chen",
  "buyer.type": "string",
  "currency": "string",
  "invoice_date": "string",
  "products": {},
  "products[].name": "Ava Chen",
  "products[].price": 1,
  "products[].quantity": 1,
  "products[].units": "string",
  "series": "string",
  "type": "string",
  "use_default_seller_info": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buyer": {},
    "buyer.country": "string",
    "buyer.first_name": "Ava",
    "buyer.last_name": "Chen",
    "buyer.type": "string",
    "currency": "string",
    "invoice_date": "string",
    "products": {},
    "products[].name": "Ava Chen",
    "products[].price": 1,
    "products[].quantity": 1,
    "products[].units": "string",
    "series": "string",
    "type": "string",
    "use_default_seller_info": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buyer` | object | yes | Buyer object. |
| `buyer.country` | string | yes | Buyer country code. |
| `buyer.first_name` | string | yes | Buyer first name. |
| `buyer.last_name` | string | yes | Buyer last name. |
| `buyer.type` | string | yes | Buyer type. |
| `currency` | string | yes | Invoice currency code. |
| `invoice_date` | string | yes | Invoice issue date. |
| `products` | list<object> | yes | Invoice line items. |
| `products[].name` | string | yes | Product or service name. |
| `products[].price` | number | yes | Product unit price. |
| `products[].quantity` | number | yes | Product quantity. |
| `products[].units` | string | yes | Units label. |
| `products[].vat_percentage` | number | no | VAT percentage for VAT invoice variants. |
| `series` | string | yes | Invoice series identifier. |
| `type` | string | yes | Invoice type enum observed from Finmei. |
| `use_default_seller_info` | boolean | yes | Whether to use the default seller information. |

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

Through the native Finmei API, this operation is `POST /invoices` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

