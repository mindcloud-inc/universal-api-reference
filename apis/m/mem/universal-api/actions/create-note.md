# Mem: Create Note

Creates a new note in Mem.

```
POST https://connect.mindcloud.co/v1/universal/mem/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mem/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mem/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The note content to save. |
| `collectionIds` | list<string> | no | Optional collection IDs to attach to the note. |
| `collectionTitles` | list<string> | no | Optional collection titles to attach to the note. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Optional note ID. |
| `createdAt` | date | no |  |
| `updatedAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collectionIds": [
        [
          "string"
        ]
      ],
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "requestId": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collectionIds[]` | array<string> | Collection IDs attached to the note. |
| `content` | string | Rendered note content. |
| `createdAt` | date | Note creation timestamp. |
| `id` | string | Mem note identifier. |
| `requestId` | string | Mem request identifier. |
| `title` | string | Note title. |
| `updatedAt` | date | Note last update timestamp. |

## Native endpoint

Through the native Mem API, this operation is `POST /v2/notes` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

