# Fatture in Cloud: Modify Product

Updates an existing product in Fatture in Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "productId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "productId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The ID of the company. |
| `productId` | number | yes | The ID of the product. |
| `data` | object | yes | The product payload inside the provider data envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultVat": {
        "description": "string",
        "id": 1,
        "isDisabled": true,
        "notes": "string",
        "value": 1
      },
      "description": "string",
      "grossPrice": 1,
      "id": 1,
      "inStock": true,
      "measure": "string",
      "name": "Ava Chen",
      "netCost": 1,
      "netPrice": 1,
      "stockCurrent": 1,
      "stockInitial": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "useGrossPrice": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `code` | string |  |
| `createdAt` | date |  |
| `defaultVat.description` | string |  |
| `defaultVat.id` | number |  |
| `defaultVat.isDisabled` | boolean |  |
| `defaultVat.notes` | string |  |
| `defaultVat.value` | number |  |
| `description` | string |  |
| `grossPrice` | number |  |
| `id` | number |  |
| `inStock` | boolean |  |
| `measure` | string |  |
| `name` | string |  |
| `netCost` | number |  |
| `netPrice` | number |  |
| `stockCurrent` | number |  |
| `stockInitial` | number |  |
| `updatedAt` | date |  |
| `useGrossPrice` | boolean |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `PUT /c/:company_id/products/:product_id` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-product.md) for the provider-specific parameters and requirements.

