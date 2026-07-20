# Shopify: Activate Inventory Item

Activates an inventory item in Shopify.

```
POST https://connect.mindcloud.co/v1/universal/shopify/latest/actions/activate-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/activate-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.inventoryItemId": "string",
  "variables.locationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/activate-inventory-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.inventoryItemId": "string",
    "variables.locationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no |  |
| `variables.inventoryItemId` | string | yes | The ID of the location of the inventory item being activated. |
| `variables.locationId` | string | yes | The ID of the location of the inventory item being activated. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiVersion` | string | no | e.g. `2026-01` As of version 2026-01, this mutation supports an optional idempotency key using the @idempotent directive. As of version 2026-04, the idempotency key is required and must be provided using the @idempotent directive. For more information, see the idempotency documentation. Default: `2026-01`. |
| `query` | string | no | This mutation __Activates an inventory item at a location with idempotency enabled__ To see all available examples [see the documentation](https://shopify.dev/docs/api/admin-graphql/latest/mutations/inventoryActivate?example=activate-an-inventory-item-at-a-location-with-idempotency-enabled-2026-01-onwards) Default: `mutation InventoryActivate(   $inventoryItemId: ID!,    $locationId: ID! ) {   inventoryActivate(     inventoryItemId: $inventoryItemId,      locationId: $locationId   ) {     inventoryLevel {       id       canDeactivate       createdAt       item {         id       }       location {         id       }       quantities(names: [\"available\"]) {         name         quantity       }       updatedAt     }   } }`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST /:apiVersion/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-inventory-item.md) for the provider-specific parameters and requirements.

