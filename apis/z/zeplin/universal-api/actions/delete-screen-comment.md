# Zeplin: Delete Screen Comment

Deletes an existing screen comment from Zeplin.

```
DELETE https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/delete-screen-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/delete-screen-comment?connectionId=$CONNECTION_ID&projectId=string&screenId=string&noteId=string&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "screenId": "string",
  "noteId": "string",
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/delete-screen-comment?${params}`, {
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
| `projectId` | string | yes | Project id |
| `screenId` | string | yes | Screen id |
| `noteId` | string | yes | Screen note id |
| `commentId` | string | yes | Screen comment id |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `DELETE /projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments/{comment_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-screen-comment.md) for the provider-specific parameters and requirements.

