# HackMD: Delete Note



```
DELETE https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/delete-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HackMD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/delete-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/delete-note?${params}`, {
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
| `noteId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HackMD API returns.

## Native endpoint

Through the native HackMD API, this operation is `DELETE /notes/:noteId` (base URL `https://api.hackmd.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-note.md) for the provider-specific parameters and requirements.

