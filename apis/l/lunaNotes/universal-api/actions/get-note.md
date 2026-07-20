# LunaNotes: Get Note

Retrieves a note from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-note?${params}`, {
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
| `id` | string | yes | The LunaNotes note ID. |
| `include` | string | no | Comma-separated: tags,video. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "draft": true,
      "icon": "string",
      "iconColor": "string",
      "id": "string",
      "isPublic": true,
      "json": {},
      "published": true,
      "status": "string",
      "timeEnd": 1,
      "timeStart": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "v": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string | Author user ID. |
| `content` | string | HTML content for the note. |
| `createdAt` | date | Timestamp when the note was created. |
| `draft` | boolean | Whether the note is still a draft. |
| `icon` | string | Note icon identifier. |
| `iconColor` | string | Note icon color. |
| `id` | string | Unique identifier for the note. |
| `isPublic` | boolean | Whether the note is publicly accessible. |
| `json` | object | Structured editor content when available. |
| `published` | boolean | Whether the note is published. |
| `status` | string | Note lifecycle status. |
| `timeEnd` | number | End time in seconds for video-linked notes. |
| `timeStart` | number | Start time in seconds for video-linked notes. |
| `title` | string | Note title. |
| `updatedAt` | date | Timestamp when the note was last updated. |
| `v` | string | Associated YouTube video ID. |
| `videoId` | string | Associated video ID. |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/notes/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

