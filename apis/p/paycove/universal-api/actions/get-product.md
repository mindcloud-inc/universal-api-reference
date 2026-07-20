# Paycove: Get Product

Retrieves a product from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product ID. Example: `1`. |

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

Through the native Paycove API, this operation is `GET products/:product_id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

