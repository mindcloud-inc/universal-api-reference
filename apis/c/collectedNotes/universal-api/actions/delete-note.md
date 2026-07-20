# Collected Notes: Delete Note



```
DELETE https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/delete-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/delete-note?connectionId=$CONNECTION_ID&siteId=1&noteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "1",
  "noteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/delete-note?${params}`, {
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
| `siteId` | number | yes | The Collected Notes site ID. |
| `noteId` | number | yes | The Collected Notes note ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Collected Notes API returns.

## Native endpoint

Through the native Collected Notes API, this operation is `DELETE /sites/:siteId/notes/:noteId` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-note.md) for the provider-specific parameters and requirements.

