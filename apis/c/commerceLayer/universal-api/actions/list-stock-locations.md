# Commerce Layer: List Stock Locations



```
GET https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-stock-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-stock-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/list-stock-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "code": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "label_format": "string",
        "name": "Ava Chen",
        "number": 1,
        "reference": "string",
        "reference_origin": "string",
        "suppress_etd": true,
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
        "address": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
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
        "stock_items": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stock_transfers": {
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
| `attributes.label_format` | string |  |
| `attributes.name` | string |  |
| `attributes.number` | number |  |
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
| `attributes.suppress_etd` | boolean |  |
| `attributes.updated_at` | date |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.mode` | string |  |
| `meta.organization_id` | string |  |
| `meta.trace_id` | string |  |
| `relationships.address.links.related` | string |  |
| `relationships.address.links.self` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.event_stores.links.related` | string |  |
| `relationships.event_stores.links.self` | string |  |
| `relationships.inventory_return_locations.links.related` | string |  |
| `relationships.inventory_return_locations.links.self` | string |  |
| `relationships.inventory_stock_locations.links.related` | string |  |
| `relationships.inventory_stock_locations.links.self` | string |  |
| `relationships.stock_items.links.related` | string |  |
| `relationships.stock_items.links.self` | string |  |
| `relationships.stock_transfers.links.related` | string |  |
| `relationships.stock_transfers.links.self` | string |  |
| `relationships.stores.links.related` | string |  |
| `relationships.stores.links.self` | string |  |
| `relationships.versions.links.related` | string |  |
| `relationships.versions.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Commerce Layer API, this operation is `GET /api/stock_locations` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-locations.md) for the provider-specific parameters and requirements.

