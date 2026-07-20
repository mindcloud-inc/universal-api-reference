# Kanban Tool: Get Board Details



```
GET https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-board-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-board-details?connectionId=$CONNECTION_ID&boardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-board-details?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "last_activity_on": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `last_activity_on` | date |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Kanban Tool API, this operation is `GET /boards/:board_id.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board-details.md) for the provider-specific parameters and requirements.

