# LunaNotes: List Summaries

Retrieves summaries from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-summaries?${params}`, {
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
| `flagged` | boolean | no | Filter by moderation status. |
| `include` | string | no | Comma-separated list of related resources to include. |
| `slug` | string | no | Filter by slug using an exact match. |
| `transcriptId` | string | no | Filter by transcript ID. |
| `videoId` | string | no | Filter by video ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "faqs": [
        {}
      ],
      "flagged": true,
      "id": "string",
      "keywords": "string",
      "slug": "string",
      "text": "string",
      "title": "string",
      "transcript": {},
      "transcriptId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "video": {},
      "videoId": "string",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `description` | string | Summary description |
| `faqs` | array<object> | FAQs linked to this summary |
| `flagged` | boolean | Moderation flag |
| `id` | string | Unique identifier for the summary |
| `keywords` | string | Summary keywords |
| `slug` | string | Summary slug |
| `text` | string | Summary text |
| `title` | string | Summary title |
| `transcript` | object | Associated transcript object |
| `transcriptId` | string | Associated transcript ID |
| `updatedAt` | date | Last update timestamp |
| `video` | object | Associated video object |
| `videoId` | string | Associated video ID |
| `views` | number | View count |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/summaries` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-summaries.md) for the provider-specific parameters and requirements.

