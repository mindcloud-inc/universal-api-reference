# Mural: List Folders for Room

Finds folders in Mural for a room.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-folders-for-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-folders-for-room?connectionId=$CONNECTION_ID&limit=25&offset=0&roomId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "roomId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/list-folders-for-room?${params}`, {
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
| `roomId` | number | yes | Unique identifier of a room. |

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

Through the native Mural API, this operation is `GET /rooms/:roomId/folders` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-folders-for-room.md) for the provider-specific parameters and requirements.

