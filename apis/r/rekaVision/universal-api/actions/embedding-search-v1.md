# Reka Vision: Embedding Search (V1)

Finds video matches in Reka Vision by embedding query.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/embedding-search-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/embedding-search-v1?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/embedding-search-v1?${params}`, {
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
| `query` | string | yes |  |
| `maxResults` | number | no |  |
| `videoIds[]` | array<string> | no |  |
| `groupIds[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threshold` | number | no |  |
| `searchDemo` | boolean | no |  |
| `useLlmRerank` | boolean | no |  |
| `useEmbedsRerank` | boolean | no |  |
| `addOcrToCaption` | boolean | no |  |
| `datetimeFrom` | string | no |  |
| `datetimeTo` | string | no |  |
| `timestampFrom` | number | no |  |
| `timestampTo` | number | no |  |
| `generateReport` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTimestamp": 1,
      "explanation": "string",
      "plainTextCaption": "string",
      "plainTextTranscript": "string",
      "s3PresignedUrl": "https://example.com",
      "score": "string",
      "startTimestamp": 1,
      "userId": "string",
      "videoChunkId": "string",
      "videoId": "string",
      "videoThumbnails": "string",
      "videoTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endTimestamp` | number | End timestamp in seconds |
| `explanation` | string | Explanation of the video chunk content and its relevance to the search query |
| `plainTextCaption` | string | Text caption for the video chunk |
| `plainTextTranscript` | string | Transcription of speech in the video chunk |
| `s3PresignedUrl` | string | Presigned S3 URL to access the parent video |
| `score` | string | Relevance score |
| `startTimestamp` | number | Start timestamp in seconds |
| `userId` | string | User ID who owns the video |
| `videoChunkId` | string | Unique identifier for the video chunk |
| `videoId` | string | Unique identifier for the video |
| `videoThumbnails` | string | URL (typically VTT) pointing to generated storyboard thumbnails |
| `videoTitle` | string | Title stored in the video's metadata |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/videos/search` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/embedding-search-v1.md) for the provider-specific parameters and requirements.

