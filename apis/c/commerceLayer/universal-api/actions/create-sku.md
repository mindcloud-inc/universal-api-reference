# Commerce Layer: Create SKU



```
POST https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-sku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-sku" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "MC-TAX-CATEGORY-SKU-001",
  "name": "MindCloud Tax Category SKU"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-sku', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "MC-TAX-CATEGORY-SKU-001",
    "name": "MindCloud Tax Category SKU"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | The SKU code. Example: `MC-TAX-CATEGORY-SKU-001`. |
| `name` | string | yes | The SKU name. Example: `MindCloud Tax Category SKU`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | no | An external reference for the SKU. Example: `MC-TAX-CATEGORY-SKU`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "do_not_ship": true,
        "do_not_track": true,
        "hs_tariff_number": "string",
        "image_url": "https://example.com",
        "jwt_custom_claim": "string",
        "name": "Ava Chen",
        "pieces_per_pack": 1,
        "reference": "string",
        "reference_origin": "string",
        "unit_of_weight": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "weight": 1
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "mode": "string",
        "organization_id": "string",
        "trace_id": "string"
      },
      "relationships": {
        "attachments": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "delivery_lead_times": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "events": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "jwt_customer": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "jwt_markets": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "jwt_stock_locations": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "links": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "prices": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shipping_category": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "sku_list_items": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "sku_lists": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "sku_options": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stock_items": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stock_reservations": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tags": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "versions": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.code` | string |  |
| `attributes.created_at` | date |  |
| `attributes.description` | string |  |
| `attributes.do_not_ship` | boolean |  |
| `attributes.do_not_track` | boolean |  |
| `attributes.hs_tariff_number` | string |  |
| `attributes.image_url` | string |  |
| `attributes.jwt_custom_claim` | string |  |
| `attributes.name` | string |  |
| `attributes.pieces_per_pack` | number |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.unit_of_weight` | string |  |
| `attributes.updated_at` | date |  |
| `attributes.weight` | number |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.delivery_lead_times.links.related` | string |  |
| `relationships.delivery_lead_times.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.jwt_customer.links.related` | string |  |
| `relationships.jwt_customer.links.self` | string |  |
| `relationships.jwt_markets.links.related` | string |  |
| `relationships.jwt_markets.links.self` | string |  |
| `relationships.jwt_stock_locations.links.related` | string |  |
| `relationships.jwt_stock_locations.links.self` | string |  |
| `relationships.links.links.related` | string |  |
| `relationships.links.links.self` | string |  |
| `relationships.prices.links.related` | string |  |
| `relationships.prices.links.self` | string |  |
| `relationships.shipping_category.links.related` | string |  |
| `relationships.shipping_category.links.self` | string |  |
| `relationships.sku_list_items.links.related` | string |  |
| `relationships.sku_list_items.links.self` | string |  |
| `relationships.sku_lists.links.related` | string |  |
| `relationships.sku_lists.links.self` | string |  |
| `relationships.sku_options.links.related` | string |  |
| `relationships.sku_options.links.self` | string |  |
| `relationships.stock_items.links.related` | string |  |
| `relationships.stock_items.links.self` | string |  |
| `relationships.stock_reservations.links.related` | string |  |
| `relationships.stock_reservations.links.self` | string |  |
| `relationships.tags.links.related` | string |  |
| `relationships.tags.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `POST /api/skus` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sku.md) for the provider-specific parameters and requirements.

