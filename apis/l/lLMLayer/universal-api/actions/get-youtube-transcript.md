# LLMLayer: Get YouTube Transcript

Retrieves a YouTube transcript from LLMLayer.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/get-youtube-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/get-youtube-transcript?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fyoutube.com%2Fwatch%3Fv%3D..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://youtube.com/watch?v=..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/get-youtube-transcript?${params}`, {
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
| `url` | string | yes | YouTube video URL. Example: `https://youtube.com/watch?v=...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "cost": 1,
      "date": "string",
      "description": "string",
      "language": "string",
      "likes": 1,
      "title": "string",
      "transcript": "string",
      "url": "https://example.com",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Video author. |
| `cost` | number | LLMLayer request cost. |
| `date` | string | Video publication date. |
| `description` | string | Video description. |
| `language` | string | Transcript language. |
| `likes` | number | Like count. |
| `title` | string | Video title. |
| `transcript` | string | Extracted YouTube transcript text. |
| `url` | string | YouTube URL. |
| `views` | number | View count. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/youtube_transcript` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-youtube-transcript.md) for the provider-specific parameters and requirements.

