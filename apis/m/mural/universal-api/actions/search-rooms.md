# Mural: Search Rooms

Finds rooms in Mural by search query.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/search-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/search-rooms?connectionId=$CONNECTION_ID&query=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/search-rooms?${params}`, {
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
| `query` | string | yes | The text this search query is for. |
| `workspaceId` | string | yes | Unique identifier of a workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /search/:workspaceId/rooms` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-rooms.md) for the provider-specific parameters and requirements.

