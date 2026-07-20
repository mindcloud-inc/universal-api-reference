# Kanban Tool: Detach Attachment



```
DELETE https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/detach-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Tool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/detach-attachment?connectionId=$CONNECTION_ID&attachmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/detach-attachment?${params}`, {
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
| `attachmentId` | number | yes | Kanban Tool attachment ID. |
| `attachable` | string | no | Optional attachable target such as `Board#100000` or `Task#200000`. Example: `Task#200000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kanban Tool API returns.

## Native endpoint

Through the native Kanban Tool API, this operation is `DELETE /attachments/:attachment_id/detach.json` (base URL `https://{{credentials.domain}}.kanbantool.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-attachment.md) for the provider-specific parameters and requirements.

