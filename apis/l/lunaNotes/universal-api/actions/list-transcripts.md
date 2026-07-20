# LunaNotes: List Transcripts

Retrieves transcripts from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-transcripts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-transcripts?${params}`, {
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
| `include` | string | no | Comma-separated list of related resources to include. |
| `kind` | string | no | Filter by transcript type or source. |
| `language` | string | no | Filter by language code such as en or es. |
| `videoId` | string | no | Filter by video ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "kind": "string",
      "language": "string",
      "name": "Ava Chen",
      "summaries": [
        {}
      ],
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "video": {},
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `id` | string | Unique identifier for the transcript |
| `kind` | string | Transcript kind |
| `language` | string | Transcript language |
| `name` | string | Transcript name |
| `summaries` | array<object> | Summaries linked to this transcript |
| `text` | string | Transcript text |
| `updatedAt` | date | Last update timestamp |
| `userId` | string | Owner user ID |
| `video` | object | Associated video object |
| `videoId` | string | Associated video ID |

## Native endpoint

Through the native LunaNotes API, this operation is `GET /v1/transcripts` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transcripts.md) for the provider-specific parameters and requirements.

