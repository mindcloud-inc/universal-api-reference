# Loyverse: List Inventory Levels

Retrieves current inventory levels from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-inventory-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-inventory-levels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-inventory-levels?${params}`, {
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
| `storeIds` | string | no | Show inventory levels only for specified stores |
| `variantIds` | string | no | Show inventory levels only for specified variants |
| `updatedAtMin` | date | no | Show inventory levels updated at or after specified date |
| `updatedAtMax` | date | no | Show inventory levels updated at or before specified date |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
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
| `cursor` | string |  |
| `inventoryLevels` | array<object> |  |
| `inventoryLevels[].inStock` | number | The current stock at the specified store |
| `inventoryLevels[].storeId` | string | The store id |
| `inventoryLevels[].updatedAt` | date | The time when specified stock was calculated |
| `inventoryLevels[].variantId` | string | The item variant id |

## Native endpoint

Through the native Loyverse API, this operation is `GET /inventory` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-levels.md) for the provider-specific parameters and requirements.

