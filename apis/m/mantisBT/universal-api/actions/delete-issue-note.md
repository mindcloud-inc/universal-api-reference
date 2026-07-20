# MantisBT: Delete Issue Note

Deletes an issue note from MantisBT.

```
DELETE https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-issue-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MantisBT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-issue-note?connectionId=$CONNECTION_ID&issueId=1&issueNoteId=1&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueId": "1",
  "issueNoteId": "1",
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mantisBT/latest/actions/delete-issue-note?${params}`, {
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
| `issueId` | number | yes | ID of the issue that owns the note |
| `issueNoteId` | number | yes | ID of the note to delete |
| `text` | string | yes | Text of the note being deleted |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MantisBT API returns.

## Native endpoint

Through the native MantisBT API, this operation is `DELETE /issues/{issue_id}/notes/{issue_note_id}` (base URL `{{credentials.baseUrl}}/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-issue-note.md) for the provider-specific parameters and requirements.

