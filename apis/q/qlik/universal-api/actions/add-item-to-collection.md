# Qlik: Add Item To Collection

Adds an item to a collection in Qlik.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/add-item-to-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/add-item-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "65b8f2a1f4b0c2d3e4f56789",
  "id": "65b8f2a1f4b0c2d3e4f56789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/add-item-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "65b8f2a1f4b0c2d3e4f56789",
    "id": "65b8f2a1f4b0c2d3e4f56789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Qlik collection ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `id` | string | yes | Item ID to add to the collection. Example: `65b8f2a1f4b0c2d3e4f56789`. |

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
      "spaceId": "string"
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

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/collections/:collectionId/items` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-item-to-collection.md) for the provider-specific parameters and requirements.

