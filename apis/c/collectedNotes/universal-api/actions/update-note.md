# Collected Notes: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": 1,
  "noteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": 1,
    "noteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | number | yes | The Collected Notes site ID. |
| `noteId` | number | yes | The Collected Notes note ID. |
| `note` | object | no |  |
| `note.body` | string | no | Markdown note content. Start with a markdown heading so Collected Notes can derive the title and path. |
| `note.visibility` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "headline": "string",
      "id": 1,
      "path": "string",
      "siteId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `createdAt` | date |  |
| `headline` | string |  |
| `id` | number |  |
| `path` | string |  |
| `siteId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Collected Notes API, this operation is `PUT /sites/:siteId/notes/:noteId` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

