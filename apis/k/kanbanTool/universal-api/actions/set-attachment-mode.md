# Kanban Tool: Set Attachment Mode



```
PUT https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/set-attachment-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/set-attachment-mode" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachmentId": 1,
  "attachable": "Task#200000",
  "mode": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/set-attachment-mode', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachmentId": 1,
    "attachable": "Task#200000",
    "mode": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentId` | number | yes | Kanban Tool attachment ID. |
| `attachable` | string | yes | Attachable target such as `Board#100000` or `Task#200000`. Example: `Task#200000`. |
| `mode` | number | yes | Mode flags: `0` none, `1` pinned, `2` cover, `3` pinned and cover. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kanban Tool API returns.

## Native endpoint

Through the native Kanban Tool API, this operation is `PATCH /attachments/:attachment_id/set_mode.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-attachment-mode.md) for the provider-specific parameters and requirements.

