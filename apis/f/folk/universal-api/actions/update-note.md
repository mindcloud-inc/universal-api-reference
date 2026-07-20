# folk: Update Note

Updates an existing note in folk.

```
PUT https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/update-note', {
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
| `noteId` | string | yes | The ID of the note to update. |
| `content` | string | no | The updated content of the note. |
| `visibility` | string | no | The updated note visibility. Supported values are public or private. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entity": {},
      "id": "string",
      "parentNote": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `content` | string |  |
| `createdAt` | date |  |
| `entity` | object |  |
| `id` | string |  |
| `parentNote` | object |  |
| `visibility` | string |  |

## Native endpoint

Through the native folk API, this operation is `PATCH /v1/notes/:noteId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

