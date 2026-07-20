# Printify: Publish Product

Publishes a product in Printify.

```
PUT https://connect.mindcloud.co/v1/universal/printify/latest/actions/publish-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printify/latest/actions/publish-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "true",
  "images": "true",
  "keyFeatures": "true",
  "product_id": "69d9640a80a288b139051dcc",
  "shipping_template": "true",
  "shop_id": "27141936",
  "tags": "true",
  "title": "true",
  "variants": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/publish-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "true",
    "images": "true",
    "keyFeatures": "true",
    "product_id": "69d9640a80a288b139051dcc",
    "shipping_template": "true",
    "shop_id": "27141936",
    "tags": "true",
    "title": "true",
    "variants": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | boolean | yes | Publish the product description. Default: `true`. |
| `images` | boolean | yes | Publish the product images. Default: `true`. |
| `keyFeatures` | boolean | yes | Publish the product key features. Default: `true`. |
| `product_id` | string | yes | Printify product id. Default: `69d9640a80a288b139051dcc`. |
| `shipping_template` | boolean | yes | Publish the shipping template. Default: `true`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |
| `tags` | boolean | yes | Publish the product tags. Default: `true`. |
| `title` | boolean | yes | Publish the product title. Default: `true`. |
| `variants` | boolean | yes | Publish the product variants. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/products/:product_id/publish.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-product.md) for the provider-specific parameters and requirements.

