# All Things Considered Podcast: Get Story Transcript

Retrieves a story transcript from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-transcript?connectionId=$CONNECTION_ID&storyId=nx-s1-5803566" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyId": "nx-s1-5803566"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-transcript?${params}`, {
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
| `storyId` | string | yes | Default: `nx-s1-5803566`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "storyId": "string",
      "title": "string",
      "transcriptText": "string",
      "transcriptUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `storyId` | string |  |
| `title` | string |  |
| `transcriptText` | string |  |
| `transcriptUrl` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /transcripts/:storyId` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-transcript.md) for the provider-specific parameters and requirements.

