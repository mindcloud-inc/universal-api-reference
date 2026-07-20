# Nuclino: Create item or collection

Creates a new item or collection in Nuclino.

```
POST https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/create-item-or-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nuclino `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/create-item-or-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/create-item-or-collection', {
  method: 'POST',
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
| `content` | string | no |  |
| `index` | string | no | Zero-based position within the parent. |
| `object` | string | no | Set to "collection" to create a collection instead of an item. |
| `parentId` | string | no |  |
| `title` | string | no |  |
| `workspaceId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nuclino API returns.

## Native endpoint

Through the native Nuclino API, this operation is `POST /items` (base URL `https://api.nuclino.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item-or-collection.md) for the provider-specific parameters and requirements.

