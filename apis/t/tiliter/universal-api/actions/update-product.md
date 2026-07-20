# Tiliter: Update Product

Updates a product in the Tiliter Recognition API.

```
PUT https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productIdPath": "string",
  "productId": "string",
  "recognitionEnabled": true,
  "productName": "Ava Chen",
  "department": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productIdPath": "string",
    "productId": "string",
    "recognitionEnabled": true,
    "productName": "Ava Chen",
    "department": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productIdPath` | string | yes |  |
| `productId` | string | yes | Product ID in the request body. Must match Product ID Path. |
| `recognitionEnabled` | boolean | yes |  |
| `productName` | string | yes |  |
| `department` | string | yes |  |
| `productDescription` | string | no |  |
| `lookupCode` | string | no |  |
| `requiredAttributes[]` | array<string> | no |  |
| `requiredAttributes[]` | array<string> | no |  |
| `optionalAttributes[]` | array<string> | no |  |
| `optionalAttributes[]` | array<string> | no |  |
| `saleMethod` | string | no |  |
| `imageUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": "string",
      "optionalAttributes": [
        "string"
      ],
      "productId": "string",
      "productName": "Ava Chen",
      "recognitionEnabled": true,
      "requiredAttributes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | string |  |
| `optionalAttributes` | array |  |
| `productId` | string |  |
| `productName` | string |  |
| `recognitionEnabled` | boolean |  |
| `requiredAttributes` | array |  |

## Native endpoint

Through the native Tiliter API, this operation is `PUT /products/:product_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

