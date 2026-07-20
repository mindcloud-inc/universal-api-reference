# Mural: Create Folder in Room

Creates a new folder in a Mural room.

```
POST https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-folder-in-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-folder-in-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-folder-in-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes |  |
| `name` | string | yes |  |
| `parentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array<object> |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Mural API, this operation is `POST /rooms/:roomId/folders` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder-in-room.md) for the provider-specific parameters and requirements.

