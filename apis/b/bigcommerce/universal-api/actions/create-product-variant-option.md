# BigCommerce: Create Product Variant Option



```
POST https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-product-variant-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-product-variant-option" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "display_name": "Ava Chen",
  "option_values[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-product-variant-option', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "display_name": "Ava Chen",
    "option_values[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | no |  |
| `type` | string<string> | yes | BigCommerce API, which determines how it will display on the storefront. Acceptable values: date, checkbox, file, text, multi_line_text, numbers_only_text, radio_buttons, rectangles, dropdown, product_list, product_list_with_images, swatch. Required in a /POST. Allowed: date \| checkbox \| file \| text \| multi_line_text \| numbers_only_text \| radio_buttons \| rectangles \| dropdown \| product_list \| product_list_with_images \| swatch |
| `display_name` | string | yes |  |
| `option_values[]` | array | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `POST /v3/catalog/products/:productId/options` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-variant-option.md) for the provider-specific parameters and requirements.

