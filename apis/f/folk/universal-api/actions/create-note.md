# folk: Create Note

Creates a new note in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "content": "string",
  "visibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "content": "string",
    "visibility": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | The ID of the entity the note belongs to. |
| `content` | string | yes | The content of the note. |
| `visibility` | string | yes | The note visibility. Supported values are public or private. |

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

Through the native folk API, this operation is `POST /v1/notes` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

