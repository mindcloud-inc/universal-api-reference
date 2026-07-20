# Mem: List Notes

Retrieves notes from Mem.

```
GET https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-notes?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Optional note ordering. |
| `filters` | object | no | Optional note filters. |
| `filters.noteVisibility` | string | no |  |
| `filters.collectionIds` | list<string> | no |  |
| `filters.containsOpenTasks` | boolean | no |  |
| `filters.containsTasks` | boolean | no |  |
| `filters.containsImages` | boolean | no |  |
| `filters.containsFiles` | boolean | no |  |
| `includeNoteContent` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": "string",
      "requestId": "string",
      "results": [
        {
          "collectionIds": [
            [
              "string"
            ]
          ],
          "content": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | string | Pagination token for the next page of notes. |
| `requestId` | string | Mem request identifier. |
| `results[].collectionIds[]` | array<string> | Collection IDs attached to the note. |
| `results[].content` | string | Rendered note content. |
| `results[].createdAt` | date | Note creation timestamp. |
| `results[].id` | string | Mem note identifier. |
| `results[].title` | string | Note title. |
| `results[].updatedAt` | date | Note last update timestamp. |

## Native endpoint

Through the native Mem API, this operation is `GET /v2/notes` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

