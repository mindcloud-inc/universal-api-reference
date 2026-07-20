# LunaNotes: Get Summary

Retrieves a summary from LunaNotes.

```
GET https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LunaNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-summary?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/get-summary?${params}`, {
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
| `id` | string | yes | The LunaNotes summary ID. |
| `include` | string | no | Include related video, transcript, or FAQs in the response |

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

Through the native LunaNotes API, this operation is `GET /v1/summaries/:id` (base URL `https://api.lunanotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-summary.md) for the provider-specific parameters and requirements.

