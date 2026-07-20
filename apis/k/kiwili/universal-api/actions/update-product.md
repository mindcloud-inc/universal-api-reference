# Kiwili: Update Product

Updates an existing product in Kiwili.

```
PUT https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the product is active. |
| `Name` | string | no | The updated product name. |
| `Price` | number | no | The updated product price. |
| `product_id` | number | yes | The Kiwili product ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Id": 1,
      "Name": "Ava Chen",
      "Price": 1,
      "SKU": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Id` | number |  |
| `Name` | string |  |
| `Price` | number |  |
| `SKU` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `PUT /product/:product_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

