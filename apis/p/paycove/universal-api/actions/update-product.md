# Paycove: Update Product

Updates a product in Paycove.

```
PUT https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product ID. Example: `1`. |
| `name` | string | no | Product name. Example: `Updated Product Name`. |
| `description` | string | no | Product description. Example: `Updated description`. |
| `amount` | number | no | Product amount. Example: `199.99`. |
| `currency` | string | no | Product currency. Example: `EUR`. |
| `salesTax` | number | no | Sales tax amount. Example: `15`. |
| `customFields` | object | no | Custom product fields object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amount": "string",
      "createdAt": "string",
      "crm": {},
      "crmCreatedAt": {},
      "crmProductId": "string",
      "crmUpdatedAt": {},
      "currency": "string",
      "description": "string",
      "foreignProduct": {},
      "id": 1,
      "name": "Ava Chen",
      "plan": {},
      "productTaxCode": "string",
      "salesTax": 1,
      "updatedAt": "string",
      "vatTax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amount` | string |  |
| `createdAt` | string |  |
| `crm` | object |  |
| `crmCreatedAt` | object |  |
| `crmProductId` | string |  |
| `crmUpdatedAt` | object |  |
| `currency` | string |  |
| `description` | string |  |
| `foreignProduct` | object |  |
| `id` | number |  |
| `name` | string |  |
| `plan` | object |  |
| `productTaxCode` | string |  |
| `salesTax` | number |  |
| `updatedAt` | string |  |
| `vatTax` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `PATCH products/:product_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

