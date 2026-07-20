# HackMD: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HackMD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "noteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noteId` | string | yes |  |
| `title` | string | no |  |
| `content` | string | no |  |
| `description` | string | no |  |
| `tags[]` | array<string> | no |  |
| `readPermission` | string | no |  |
| `writePermission` | string | no |  |
| `parentFolderId` | string | no |  |
| `permalink` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HackMD API returns.

## Native endpoint

Through the native HackMD API, this operation is `PATCH /notes/:noteId` (base URL `https://api.hackmd.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

