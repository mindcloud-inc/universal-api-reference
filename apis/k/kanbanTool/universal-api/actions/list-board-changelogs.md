# Kanban Tool: List Board Changelogs



```
GET https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/list-board-changelogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/list-board-changelogs?connectionId=$CONNECTION_ID&boardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/list-board-changelogs?${params}`, {
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
| `boardId` | number | yes | Kanban Tool board ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | number | no | Only return changelogs with an ID smaller than this value. Example: `500000`. |
| `after` | number | no | Only return changelogs with an ID greater than this value. Example: `500000`. |
| `limit` | number | no | Maximum number of changelog entries to return. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board_id": 1,
      "changed_object_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "what": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board_id` | number |  |
| `changed_object_type` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `what` | string |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `GET /boards/:board_id/changelog.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-changelogs.md) for the provider-specific parameters and requirements.

