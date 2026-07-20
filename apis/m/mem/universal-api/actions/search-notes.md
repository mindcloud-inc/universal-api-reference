# Mem: Search Notes

Finds notes in Mem by search query.

```
GET https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-notes?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem/latest/actions/search-notes?${params}`, {
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
| `query` | string | yes | Search query text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no | Optional search filters. |
| `filters.byCollectionIds` | list<string> | no |  |
| `filters.containsOpenTasks` | boolean | no |  |
| `filters.containsTasks` | boolean | no |  |
| `filters.containsImages` | boolean | no |  |
| `filters.containsFiles` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
          "snippet": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Mem request identifier. |
| `results[].collectionIds[]` | array<string> | Collection IDs attached to the note. |
| `results[].content` | string | Rendered note content. |
| `results[].createdAt` | date | Note creation timestamp. |
| `results[].id` | string | Mem note identifier. |
| `results[].snippet` | string | Search snippet for the matching note. |
| `results[].title` | string | Note title. |
| `results[].updatedAt` | date | Note last update timestamp. |
| `total` | number | Total matching notes. |

## Native endpoint

Through the native Mem API, this operation is `POST /v2/notes/search` (base URL `https://api.mem.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-notes.md) for the provider-specific parameters and requirements.

