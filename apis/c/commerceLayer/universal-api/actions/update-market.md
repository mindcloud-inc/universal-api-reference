# Commerce Layer: Update Market



```
PUT https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-market
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-market" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "QlNQVhbvgD",
  "resourceId": "QlNQVhbvgD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/update-market', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "QlNQVhbvgD",
    "resourceId": "QlNQVhbvgD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The market ID to update. Example: `QlNQVhbvgD`. |
| `resourceId` | string | yes | The market resource ID in the JSON:API body. Use the same value as Market ID. Example: `QlNQVhbvgD`. |
| `name` | string | no | The updated market name. Example: `MindCloud Updated Market`. |
| `code` | string | no | The updated market code. Example: `mindcloud-updated-market`. |
| `reference` | string | no | The updated external reference. Example: `MC-UPDATED-MARKET`. |
| `referenceOrigin` | string | no | The updated reference origin. Example: `mindcloud-wizard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "checkout_url": "https://example.com",
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "disabled_at": "2026-05-07T12:00:00.000Z",
        "external_includes": [
          "string"
        ],
        "external_order_validation_url": "https://example.com",
        "external_prices_url": "https://example.com",
        "facebook_pixel_id": "string",
        "name": "Ava Chen",
        "number": 1,
        "private": true,
        "reference": "string",
        "reference_origin": "string",
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
| `attributes.checkout_url` | string |  |
| `attributes.code` | string |  |
| `attributes.created_at` | date |  |
| `attributes.disabled_at` | date |  |
| `attributes.external_includes[]` | string |  |
| `attributes.external_order_validation_url` | string |  |
| `attributes.external_prices_url` | string |  |
| `attributes.facebook_pixel_id` | string |  |
| `attributes.name` | string |  |
| `attributes.number` | number |  |
| `attributes.private` | boolean |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
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

Through the native Commerce Layer API, this operation is `PATCH /api/markets/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-market.md) for the provider-specific parameters and requirements.

