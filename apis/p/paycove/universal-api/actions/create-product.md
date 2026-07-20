# Paycove: Create Product

Creates a product in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Product name. |
| `description` | string | no | Product description. |
| `crmProductId` | string | no | External CRM product identifier. |
| `amount` | number | no | Product amount. |
| `currency` | string | no | Three-letter currency code. |
| `productTaxCode` | string | no | Product tax code. |
| `salesTax` | number | no | Sales tax percentage. |
| `vatTax` | number | no | VAT tax percentage. |
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

Through the native Paycove API, this operation is `POST products` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

