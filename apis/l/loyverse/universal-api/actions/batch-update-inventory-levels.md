# Loyverse: Batch Update Inventory Levels

Updates inventory levels in batch in Loyverse.

```
PUT https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/batch-update-inventory-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/batch-update-inventory-levels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/batch-update-inventory-levels', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventoryLevels[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryLevels": [
        {
          "inStock": 1,
          "storeId": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "variantId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryLevels` | array<object> |  |
| `inventoryLevels[].inStock` | number | The current stock at the specified store |
| `inventoryLevels[].storeId` | string | The store id |
| `inventoryLevels[].updatedAt` | date | The time when specified stock was calculated |
| `inventoryLevels[].variantId` | string | The item variant id |

## Native endpoint

Through the native Loyverse API, this operation is `POST /inventory` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-inventory-levels.md) for the provider-specific parameters and requirements.

