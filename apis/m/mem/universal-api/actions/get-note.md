# Mem: Get Note

Retrieves a note from Mem.

```
GET https://connect.mindcloud.co/v1/universal/mem/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/get-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem/latest/actions/get-note?${params}`, {
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

Through the native Mem API, this operation is `GET /v2/notes/:noteId` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

