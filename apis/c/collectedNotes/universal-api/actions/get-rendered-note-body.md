# Collected Notes: Get Rendered Note Body



```
GET https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-rendered-note-body
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Collected Notes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-rendered-note-body?connectionId=$CONNECTION_ID&siteId=1&noteId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "1",
  "noteId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-rendered-note-body?${params}`, {
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
| `siteId` | number | yes |  |
| `noteId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "note": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `note.body` | string |  |
| `note.createdAt` | date |  |
| `note.headline` | string |  |
| `note.id` | number |  |
| `note.path` | string |  |
| `note.siteId` | number |  |
| `note.title` | string |  |
| `note.updatedAt` | date |  |
| `note.url` | string |  |
| `note.userId` | number |  |
| `note.visibility` | string |  |

## Native endpoint

Through the native Collected Notes API, this operation is `GET /sites/:siteId/notes/:noteId/body` (base URL `https://collectednotes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rendered-note-body.md) for the provider-specific parameters and requirements.

