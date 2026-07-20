# Kanban Tool: Search Tasks



```
GET https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/search-tasks?connectionId=$CONNECTION_ID&q=priority%3A1%20%40jd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "priority:1 @jd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/search-tasks?${params}`, {
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
| `q` | string | yes | Search query. Required by the API, but it may be an empty string. Example: `priority:1 @jd`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of tasks to return, or tasks per page when `page` is also supplied. Example: `25`. |
| `page` | number | no | Page number. When set, the API returns pagination metadata together with results. Example: `1`. |
| `boardIds` | string | no | Comma-separated list of board IDs to narrow the search scope. Example: `100000,100001`. |
| `archived` | number | no | Set to `1` to search archived tasks. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "2026-05-07T12:00:00.000Z",
      "board_id": 1,
      "card_color_in_rgb": "string",
      "card_color_invert": true,
      "card_type_color_ref": "string",
      "card_type_name": "Ava Chen",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | date |  |
| `board_id` | number |  |
| `card_color_in_rgb` | string |  |
| `card_color_invert` | boolean |  |
| `card_type_color_ref` | string |  |
| `card_type_name` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `GET /tasks/search.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.

