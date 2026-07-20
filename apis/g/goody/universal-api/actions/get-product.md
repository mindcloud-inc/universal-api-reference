# Goody: Get Product

Retrieves a specific product from Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | Product ID |
| `useCustomCatalog` | boolean | no | Limit to custom catalog only (for approved API partners) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        "string"
      ],
      "brand": {
        "brand_values": [
          "string"
        ],
        "free_shipping_minimum": "string",
        "id": "string",
        "name": "Ava Chen",
        "shipping_price": 1
      },
      "id": "string",
      "images": [
        "string"
      ],
      "name": "Ava Chen",
      "price": 1,
      "price_is_variable": true,
      "recipient_description": "string",
      "restricted_states": [
        "string"
      ],
      "status": "string",
      "subtitle": "string",
      "subtitle_short": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "variant_groups": [
        "string"
      ],
      "variants": {
        "id": "string",
        "image_large": "string",
        "name": "Ava Chen",
        "subtitle": "string"
      },
      "variants_label": "string",
      "variants_num_selectable": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<string> |  |
| `brand` | object |  |
| `brand.brand_values` | array<string> |  |
| `brand.free_shipping_minimum` | string |  |
| `brand.id` | string |  |
| `brand.name` | string |  |
| `brand.shipping_price` | number |  |
| `id` | string |  |
| `images` | array<string> |  |
| `name` | string |  |
| `price` | number |  |
| `price_is_variable` | boolean |  |
| `recipient_description` | string |  |
| `restricted_states` | array<string> |  |
| `status` | string |  |
| `subtitle` | string |  |
| `subtitle_short` | string |  |
| `updated_at` | date |  |
| `variant_groups` | array<string> |  |
| `variants` | array<object> |  |
| `variants_label` | string |  |
| `variants_num_selectable` | number |  |
| `variants.id` | string |  |
| `variants.image_large` | string |  |
| `variants.name` | string |  |
| `variants.subtitle` | string |  |

## Native endpoint

Through the native Goody API, this operation is `GET /v1/products/:id` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

