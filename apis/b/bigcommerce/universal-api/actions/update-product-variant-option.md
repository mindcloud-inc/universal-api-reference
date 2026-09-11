# BigCommerce: Update Product Variant Option



```
PUT https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant-option" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "type": "string",
  "optionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/update-product-variant-option', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "type": "string",
    "optionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes |  |
| `type` | string<string> | yes | BigCommerce API, which determines how it will display on the storefront. Acceptable values: date, checkbox, file, text, multi_line_text, numbers_only_text, radio_buttons, rectangles, dropdown, product_list, product_list_with_images, swatch. Required in a /POST. Allowed: date \| checkbox \| file \| text \| multi_line_text \| numbers_only_text \| radio_buttons \| rectangles \| dropdown \| product_list \| product_list_with_images \| swatch |
| `display_name` | string | no |  |
| `option_values[]` | array | no |  |
| `optionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `PUT /v3/catalog/products/:productId/options/:optionId` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-variant-option.md) for the provider-specific parameters and requirements.

