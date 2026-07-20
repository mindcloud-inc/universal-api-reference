# YouCan: Create Order

Creates a new order in YouCan.

```
POST https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youCan/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "discount": {
        "id": "string",
        "reason": "string",
        "type": 1,
        "type_text": "string",
        "value": 1
      },
      "extra_fields": "string",
      "id": "string",
      "is_refunded_by_platform": true,
      "links": {
        "edit": "https://example.com",
        "self": "https://example.com"
      },
      "notes": "string",
      "payment": {
        "address": [
          "string"
        ],
        "created_at": "2026-05-07T12:00:00.000Z",
        "payload": {
          "gateway": "string"
        },
        "status": 1,
        "status_text": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "platform_fee": 1,
      "ref": "string",
      "refunds": [
        "string"
      ],
      "shipping": {
        "address": {
          "city": "string",
          "company": "string",
          "country_code": "string",
          "country_name": "Ava Chen",
          "created_at": 1,
          "default": true,
          "first_line": "string",
          "first_name": "Ava",
          "full_name": "Ava Chen",
          "id": "string",
          "last_name": "Chen",
          "phone": "string",
          "region": "string",
          "second_line": "string",
          "state": "string",
          "updated_at": 1,
          "zip_code": "string"
        },
        "created_at": "2026-05-07T12:00:00.000Z",
        "is_free": true,
        "payload": {
          "compound_id": "string",
          "display_name": "Ava Chen",
          "id": "string",
          "instance_class_name": "Ava Chen",
          "is_active": true,
          "is_free": true,
          "name": "Ava Chen",
          "price": 1
        },
        "price": 1,
        "status": 1,
        "status_text": "string",
        "tracking_number": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "status": 1,
      "tags": [
        "string"
      ],
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "variants": [
        {
          "created_at": 1,
          "extra_fields": [
            "string"
          ],
          "id": "string",
          "price": 1,
          "quantity": 1,
          "updated_at": 1,
          "variant": {
            "barcode": "string",
            "compare_at_price": 1,
            "created_at": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "image": {
              "name": "Ava Chen",
              "url": "https://example.com"
            },
            "inventory": 1,
            "is_default": true,
            "is_selected": true,
            "options": [
              "string"
            ],
            "price": 1,
            "product": {
              "advanced_options": {
                "enabled": true,
                "related_products": [
                  "string"
                ]
              },
              "compare_at_price": 1,
              "cost_price": "string",
              "created_at": "2026-05-07T12:00:00.000Z",
              "deleted_at": true,
              "description": "string",
              "has_variants": true,
              "id": "string",
              "images": [
                {
                  "id": "string",
                  "name": "Ava Chen",
                  "order": 1,
                  "type": 1,
                  "url": "https://example.com",
                  "variations": {
                    "lg": "string",
                    "md": "string",
                    "original": "string",
                    "sm": "string"
                  }
                }
              ],
              "inventory": 1,
              "meta": {
                "description": "string",
                "images": [
                  {
                    "link": "https://example.com",
                    "path": "string"
                  }
                ],
                "title": "string"
              },
              "name": "Ava Chen",
              "price": 1,
              "public_url": "https://example.com",
              "slug": "string",
              "thumbnail": "string",
              "track_inventory": true,
              "updated_at": "2026-05-07T12:00:00.000Z",
              "variant_options": [
                "string"
              ],
              "variants_count": 1,
              "visibility": true
            },
            "sku": "string",
            "updated_at": "2026-05-07T12:00:00.000Z",
            "values": [
              "string"
            ],
            "variations": {
              "default": "string"
            },
            "weight": 1
          }
        }
      ],
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `discount` | object |  |
| `discount.id` | string |  |
| `discount.reason` | string |  |
| `discount.type` | number |  |
| `discount.type_text` | string |  |
| `discount.value` | number |  |
| `extra_fields` | string |  |
| `id` | string |  |
| `is_refunded_by_platform` | boolean |  |
| `links` | object |  |
| `links.edit` | string |  |
| `links.self` | string |  |
| `notes` | string |  |
| `payment` | object |  |
| `payment.address` | array |  |
| `payment.created_at` | date |  |
| `payment.payload` | object |  |
| `payment.payload.gateway` | string |  |
| `payment.status` | number |  |
| `payment.status_text` | string |  |
| `payment.updated_at` | date |  |
| `platform_fee` | number |  |
| `ref` | string |  |
| `refunds` | array |  |
| `shipping` | object |  |
| `shipping.address` | object |  |
| `shipping.address.city` | string |  |
| `shipping.address.company` | string |  |
| `shipping.address.country_code` | string |  |
| `shipping.address.country_name` | string |  |
| `shipping.address.created_at` | number |  |
| `shipping.address.default` | boolean |  |
| `shipping.address.first_line` | string |  |
| `shipping.address.first_name` | string |  |
| `shipping.address.full_name` | string |  |
| `shipping.address.id` | string |  |
| `shipping.address.last_name` | string |  |
| `shipping.address.phone` | string |  |
| `shipping.address.region` | string |  |
| `shipping.address.second_line` | string |  |
| `shipping.address.state` | string |  |
| `shipping.address.updated_at` | number |  |
| `shipping.address.zip_code` | string |  |
| `shipping.created_at` | date |  |
| `shipping.is_free` | boolean |  |
| `shipping.payload` | object |  |
| `shipping.payload.compound_id` | string |  |
| `shipping.payload.display_name` | string |  |
| `shipping.payload.id` | string |  |
| `shipping.payload.instance_class_name` | string |  |
| `shipping.payload.is_active` | boolean |  |
| `shipping.payload.is_free` | boolean |  |
| `shipping.payload.name` | string |  |
| `shipping.payload.price` | number |  |
| `shipping.price` | number |  |
| `shipping.status` | number |  |
| `shipping.status_text` | string |  |
| `shipping.tracking_number` | string |  |
| `shipping.updated_at` | date |  |
| `status` | number |  |
| `tags` | array<string> |  |
| `total` | number |  |
| `updated_at` | date |  |
| `variants` | array<object> |  |
| `variants[].created_at` | number |  |
| `variants[].extra_fields` | array |  |
| `variants[].id` | string |  |
| `variants[].price` | number |  |
| `variants[].quantity` | number |  |
| `variants[].updated_at` | number |  |
| `variants[].variant` | object |  |
| `variants[].variant.barcode` | string |  |
| `variants[].variant.compare_at_price` | number |  |
| `variants[].variant.created_at` | date |  |
| `variants[].variant.id` | string |  |
| `variants[].variant.image` | object |  |
| `variants[].variant.image.name` | string |  |
| `variants[].variant.image.url` | string |  |
| `variants[].variant.inventory` | number |  |
| `variants[].variant.is_default` | boolean |  |
| `variants[].variant.is_selected` | boolean |  |
| `variants[].variant.options` | array<string> |  |
| `variants[].variant.price` | number |  |
| `variants[].variant.product` | object |  |
| `variants[].variant.product.advanced_options` | object |  |
| `variants[].variant.product.advanced_options.enabled` | boolean |  |
| `variants[].variant.product.advanced_options.related_products` | array |  |
| `variants[].variant.product.compare_at_price` | number |  |
| `variants[].variant.product.cost_price` | string |  |
| `variants[].variant.product.created_at` | date |  |
| `variants[].variant.product.deleted_at` | boolean |  |
| `variants[].variant.product.description` | string |  |
| `variants[].variant.product.has_variants` | boolean |  |
| `variants[].variant.product.id` | string |  |
| `variants[].variant.product.images` | array<object> |  |
| `variants[].variant.product.images[].id` | string |  |
| `variants[].variant.product.images[].name` | string |  |
| `variants[].variant.product.images[].order` | number |  |
| `variants[].variant.product.images[].type` | number |  |
| `variants[].variant.product.images[].url` | string |  |
| `variants[].variant.product.images[].variations` | object |  |
| `variants[].variant.product.images[].variations.lg` | string |  |
| `variants[].variant.product.images[].variations.md` | string |  |
| `variants[].variant.product.images[].variations.original` | string |  |
| `variants[].variant.product.images[].variations.sm` | string |  |
| `variants[].variant.product.inventory` | number |  |
| `variants[].variant.product.meta` | object |  |
| `variants[].variant.product.meta.description` | string |  |
| `variants[].variant.product.meta.images` | array<object> |  |
| `variants[].variant.product.meta.images[].link` | string |  |
| `variants[].variant.product.meta.images[].path` | string |  |
| `variants[].variant.product.meta.title` | string |  |
| `variants[].variant.product.name` | string |  |
| `variants[].variant.product.price` | number |  |
| `variants[].variant.product.public_url` | string |  |
| `variants[].variant.product.slug` | string |  |
| `variants[].variant.product.thumbnail` | string |  |
| `variants[].variant.product.track_inventory` | boolean |  |
| `variants[].variant.product.updated_at` | date |  |
| `variants[].variant.product.variant_options` | array |  |
| `variants[].variant.product.variants_count` | number |  |
| `variants[].variant.product.visibility` | boolean |  |
| `variants[].variant.sku` | string |  |
| `variants[].variant.updated_at` | date |  |
| `variants[].variant.values` | array<string> |  |
| `variants[].variant.variations` | object |  |
| `variants[].variant.variations.default` | string |  |
| `variants[].variant.weight` | number |  |
| `vat` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `POST /orders` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

