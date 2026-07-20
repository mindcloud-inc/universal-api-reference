# Qlik: Update Item

Updates an existing item in Qlik.

```
PUT https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "65b8f2a1f4b0c2d3e4f56789",
  "resourceType": "app"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "65b8f2a1f4b0c2d3e4f56789",
    "resourceType": "app"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | Qlik item ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `resourceType` | string | yes | Qlik item resource type. Example: `app`. |
| `name` | string | no | Item name. Example: `Sales dashboard`. |
| `spaceId` | string | no | Space ID for the item. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "resourceType": "string",
      "spaceId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `resourceType` | string |  |
| `spaceId` | string |  |
| `tenantId` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `PUT /api/v1/items/:itemId` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

