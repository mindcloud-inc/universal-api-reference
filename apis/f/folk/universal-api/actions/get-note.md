# folk: Get Note

Retrieves a specific note from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/get-note?${params}`, {
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
| `noteId` | string | yes | The ID of the note to retrieve. |

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

Through the native folk API, this operation is `GET /v1/notes/:noteId` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

