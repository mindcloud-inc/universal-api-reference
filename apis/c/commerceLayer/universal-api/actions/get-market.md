# Commerce Layer: Get Market



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-market
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-market?connectionId=$CONNECTION_ID&id=VgWXOhKylz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "VgWXOhKylz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-market?${params}`, {
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
| `id` | string | yes | The ID of the market to retrieve. Example: `VgWXOhKylz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "external_includes": [
          "string"
        ],
        "name": "Ava Chen",
        "number": 1,
        "private": true,
        "shared_secret": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
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
        "base_price_list": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "customer_group": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "default_payment_method": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "default_shipping_method": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "discount_engine": {
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
        "geocoder": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "inventory_model": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "merchant": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "order_validation_rules": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "price_list_schedulers": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "price_list": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "subscription_model": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "tax_calculator": {
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
| `attributes.created_at` | date |  |
| `attributes.external_includes[]` | string |  |
| `attributes.name` | string |  |
| `attributes.number` | number |  |
| `attributes.private` | boolean |  |
| `attributes.shared_secret` | string |  |
| `attributes.updated_at` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.base_price_list.links.related` | string |  |
| `relationships.base_price_list.links.self` | string |  |
| `relationships.customer_group.links.related` | string |  |
| `relationships.customer_group.links.self` | string |  |
| `relationships.default_payment_method.links.related` | string |  |
| `relationships.default_payment_method.links.self` | string |  |
| `relationships.default_shipping_method.links.related` | string |  |
| `relationships.default_shipping_method.links.self` | string |  |
| `relationships.discount_engine.links.related` | string |  |
| `relationships.discount_engine.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.geocoder.links.related` | string |  |
| `relationships.geocoder.links.self` | string |  |
| `relationships.inventory_model.links.related` | string |  |
| `relationships.inventory_model.links.self` | string |  |
| `relationships.merchant.links.related` | string |  |
| `relationships.merchant.links.self` | string |  |
| `relationships.order_validation_rules.links.related` | string |  |
| `relationships.order_validation_rules.links.self` | string |  |
| `relationships.price_list_schedulers.links.related` | string |  |
| `relationships.price_list_schedulers.links.self` | string |  |
| `relationships.price_list.links.related` | string |  |
| `relationships.price_list.links.self` | string |  |
| `relationships.stores.links.related` | string |  |
| `relationships.stores.links.self` | string |  |
| `relationships.subscription_model.links.related` | string |  |
| `relationships.subscription_model.links.self` | string |  |
| `relationships.tax_calculator.links.related` | string |  |
| `relationships.tax_calculator.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `GET /api/markets/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market.md) for the provider-specific parameters and requirements.

