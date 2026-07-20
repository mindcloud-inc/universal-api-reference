# LunaNotes: Get Transcript

Retrieves a transcript from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-transcript?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-transcript?${params}`, {
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
| `id` | string | yes | The LunaNotes transcript ID. |
| `include` | string | no | Include related video or summaries in the response |

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

Through the native LunaNotes API, this operation is `GET /v1/transcripts/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

