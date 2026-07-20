# ForceManager: Create Product

Creates a new product in ForceManager.

```
POST https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "price": 1,
  "categoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "price": 1,
    "categoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Name of the product. |
| `price` | number | yes | Selling price for the product. |
| `categoryId` | number | yes | ID of the category for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "description": "string",
      "extId": "string",
      "id": 1,
      "model": "string",
      "notAvailable": true,
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number | ID of the category of the product. |
| `description` | string | Comment for the product. |
| `extId` | string | External id of the product from a third-party system. |
| `id` | number | Unique identifier for the product. |
| `model` | string | Name of the product. |
| `notAvailable` | boolean | Whether the product is not available. |
| `price` | number | Selling price for the product. |

## Native endpoint

Through the native ForceManager API, this operation is `POST /products`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

