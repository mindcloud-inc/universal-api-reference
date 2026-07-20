# Commerce Layer: Get Inventory Model



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-inventory-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-inventory-model?connectionId=$CONNECTION_ID&id=AZrjASxYZY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "AZrjASxYZY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/get-inventory-model?${params}`, {
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
| `id` | string | yes | The ID of the inventory model to retrieve. Example: `AZrjASxYZY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "manual_stock_decrement": true,
        "name": "Ava Chen",
        "put_stock_transfers_on_hold": true,
        "stock_locations_cutoff": 1,
        "stock_reservation_cutoff": 1,
        "strategy": "string",
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
        "event_stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "inventory_return_locations": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "inventory_stock_locations": {
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
| `attributes.manual_stock_decrement` | boolean |  |
| `attributes.name` | string |  |
| `attributes.put_stock_transfers_on_hold` | boolean |  |
| `attributes.stock_locations_cutoff` | number |  |
| `attributes.stock_reservation_cutoff` | number |  |
| `attributes.strategy` | string |  |
| `attributes.updated_at` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.inventory_return_locations.links.related` | string |  |
| `relationships.inventory_return_locations.links.self` | string |  |
| `relationships.inventory_stock_locations.links.related` | string |  |
| `relationships.inventory_stock_locations.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `GET /api/inventory_models/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-model.md) for the provider-specific parameters and requirements.

