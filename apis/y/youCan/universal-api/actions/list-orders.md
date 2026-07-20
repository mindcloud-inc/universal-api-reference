# YouCan: List Orders

Retrieves a list of orders from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-orders?${params}`, {
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
| `limit` | string | no |  |
| `page` | string | no |  |
| `q` | string | no |  |
| `sort_field` | string | no |  |
| `sort_order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
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
              "gateway": "string",
              "gateway_id": "string",
              "note": "string",
              "thank-you-message": "string"
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
            "address": [
              "string"
            ],
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
            "shipping_zone_id": "string",
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
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {
            "next": "https://example.com"
          },
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].created_at` | date |  |
| `data[].extra_fields` | string |  |
| `data[].id` | string |  |
| `data[].is_refunded_by_platform` | boolean |  |
| `data[].links` | object |  |
| `data[].links.edit` | string |  |
| `data[].links.self` | string |  |
| `data[].notes` | string |  |
| `data[].payment` | object |  |
| `data[].payment.address` | array |  |
| `data[].payment.created_at` | date |  |
| `data[].payment.payload` | object |  |
| `data[].payment.payload.gateway` | string |  |
| `data[].payment.payload.gateway_id` | string |  |
| `data[].payment.payload.note` | string |  |
| `data[].payment.payload.thank-you-message` | string |  |
| `data[].payment.status` | number |  |
| `data[].payment.status_text` | string |  |
| `data[].payment.updated_at` | date |  |
| `data[].platform_fee` | number |  |
| `data[].ref` | string |  |
| `data[].refunds` | array |  |
| `data[].shipping` | object |  |
| `data[].shipping.address` | array |  |
| `data[].shipping.created_at` | date |  |
| `data[].shipping.is_free` | boolean |  |
| `data[].shipping.payload` | object |  |
| `data[].shipping.payload.compound_id` | string |  |
| `data[].shipping.payload.display_name` | string |  |
| `data[].shipping.payload.id` | string |  |
| `data[].shipping.payload.instance_class_name` | string |  |
| `data[].shipping.payload.is_active` | boolean |  |
| `data[].shipping.payload.is_free` | boolean |  |
| `data[].shipping.payload.name` | string |  |
| `data[].shipping.payload.price` | number |  |
| `data[].shipping.price` | number |  |
| `data[].shipping.shipping_zone_id` | string |  |
| `data[].shipping.status` | number |  |
| `data[].shipping.status_text` | string |  |
| `data[].shipping.tracking_number` | string |  |
| `data[].shipping.updated_at` | date |  |
| `data[].status` | number |  |
| `data[].tags` | array |  |
| `data[].total` | number |  |
| `data[].updated_at` | date |  |
| `data[].variants` | array<object> |  |
| `data[].variants[].created_at` | number |  |
| `data[].variants[].extra_fields` | array |  |
| `data[].variants[].id` | string |  |
| `data[].variants[].price` | number |  |
| `data[].variants[].quantity` | number |  |
| `data[].variants[].updated_at` | number |  |
| `data[].variants[].variant` | object |  |
| `data[].variants[].variant.barcode` | string |  |
| `data[].variants[].variant.compare_at_price` | number |  |
| `data[].variants[].variant.created_at` | date |  |
| `data[].variants[].variant.id` | string |  |
| `data[].variants[].variant.image` | object |  |
| `data[].variants[].variant.image.name` | string |  |
| `data[].variants[].variant.image.url` | string |  |
| `data[].variants[].variant.inventory` | number |  |
| `data[].variants[].variant.is_default` | boolean |  |
| `data[].variants[].variant.is_selected` | boolean |  |
| `data[].variants[].variant.options` | array<string> |  |
| `data[].variants[].variant.price` | number |  |
| `data[].variants[].variant.product` | object |  |
| `data[].variants[].variant.product.advanced_options` | object |  |
| `data[].variants[].variant.product.advanced_options.enabled` | boolean |  |
| `data[].variants[].variant.product.advanced_options.related_products` | array |  |
| `data[].variants[].variant.product.compare_at_price` | number |  |
| `data[].variants[].variant.product.cost_price` | string |  |
| `data[].variants[].variant.product.created_at` | date |  |
| `data[].variants[].variant.product.deleted_at` | boolean |  |
| `data[].variants[].variant.product.description` | string |  |
| `data[].variants[].variant.product.has_variants` | boolean |  |
| `data[].variants[].variant.product.id` | string |  |
| `data[].variants[].variant.product.images` | array<object> |  |
| `data[].variants[].variant.product.images[].id` | string |  |
| `data[].variants[].variant.product.images[].name` | string |  |
| `data[].variants[].variant.product.images[].order` | number |  |
| `data[].variants[].variant.product.images[].type` | number |  |
| `data[].variants[].variant.product.images[].url` | string |  |
| `data[].variants[].variant.product.images[].variations` | object |  |
| `data[].variants[].variant.product.images[].variations.lg` | string |  |
| `data[].variants[].variant.product.images[].variations.md` | string |  |
| `data[].variants[].variant.product.images[].variations.original` | string |  |
| `data[].variants[].variant.product.images[].variations.sm` | string |  |
| `data[].variants[].variant.product.inventory` | number |  |
| `data[].variants[].variant.product.meta` | object |  |
| `data[].variants[].variant.product.meta.description` | string |  |
| `data[].variants[].variant.product.meta.images` | array<object> |  |
| `data[].variants[].variant.product.meta.images[].link` | string |  |
| `data[].variants[].variant.product.meta.images[].path` | string |  |
| `data[].variants[].variant.product.meta.title` | string |  |
| `data[].variants[].variant.product.name` | string |  |
| `data[].variants[].variant.product.price` | number |  |
| `data[].variants[].variant.product.public_url` | string |  |
| `data[].variants[].variant.product.slug` | string |  |
| `data[].variants[].variant.product.thumbnail` | string |  |
| `data[].variants[].variant.product.track_inventory` | boolean |  |
| `data[].variants[].variant.product.updated_at` | date |  |
| `data[].variants[].variant.product.variant_options` | array |  |
| `data[].variants[].variant.product.variants_count` | number |  |
| `data[].variants[].variant.product.visibility` | boolean |  |
| `data[].variants[].variant.sku` | string |  |
| `data[].variants[].variant.updated_at` | date |  |
| `data[].variants[].variant.values` | array<string> |  |
| `data[].variants[].variant.variations` | object |  |
| `data[].variants[].variant.variations.default` | string |  |
| `data[].variants[].variant.weight` | number |  |
| `data[].vat` | number |  |
| `meta` | object |  |
| `meta.pagination` | object |  |
| `meta.pagination.count` | number |  |
| `meta.pagination.current_page` | number |  |
| `meta.pagination.links` | object |  |
| `meta.pagination.links.next` | string |  |
| `meta.pagination.per_page` | number |  |
| `meta.pagination.total` | number |  |
| `meta.pagination.total_pages` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /orders` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

