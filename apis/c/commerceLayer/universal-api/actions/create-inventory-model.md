# Commerce Layer: Create Inventory Model



```
POST https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-inventory-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-inventory-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "EU Inventory Model"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/create-inventory-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "EU Inventory Model"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The inventory model name. Example: `EU Inventory Model`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `strategy` | string | no | The inventory split strategy. Default: `no_split`. Example: `no_split`. |
| `stockLocationsCutoff` | number | no | The stock locations cutoff value. Default: `2`. Example: `2`. |
| `stockReservationCutoff` | number | no | The stock reservation cutoff in seconds. Default: `3600`. Example: `3600`. |
| `putStockTransfersOnHold` | boolean | no | Whether stock transfers should be put on hold. Default: `false`. Example: `false`. |
| `manualStockDecrement` | boolean | no | Whether stock decrement should be handled manually. Default: `false`. Example: `false`. |
| `reference` | string | no | An external reference for the inventory model. Example: `ANY-EXTERNAL-REFERENCE`. |
| `referenceOrigin` | string | no | The origin of the external reference. Example: `ANY-EXTERNAL-REFERENCE-ORIGIN`. |

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
        "reference": "string",
        "reference_origin": "string",
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
| `attributes.reference` | string |  |
| `attributes.reference_origin` | string |  |
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

Through the native Commerce Layer API, this operation is `POST /api/inventory_models` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inventory-model.md) for the provider-specific parameters and requirements.

