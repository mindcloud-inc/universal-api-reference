# All Things Considered Podcast: Get Story Details

Retrieves story details from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-details?connectionId=$CONNECTION_ID&year=2026&month=04&day=29&storyId=nx-s1-5803566&slug=musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026",
  "month": "04",
  "day": "29",
  "storyId": "nx-s1-5803566",
  "slug": "musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-details?${params}`, {
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
| `year` | string | yes | Default: `2026`. |
| `month` | string | yes | Default: `04`. |
| `day` | string | yes | Default: `29`. |
| `storyId` | string | yes | Default: `nx-s1-5803566`. |
| `slug` | string | yes | Default: `musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "author": "string",
      "canonicalUrl": "https://example.com",
      "description": "string",
      "duration": 1,
      "imageUrl": "https://example.com",
      "mediaId": "string",
      "publishDateTime": "string",
      "storyId": "string",
      "title": "string",
      "topic": "string",
      "transcriptUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string |  |
| `author` | string |  |
| `canonicalUrl` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `imageUrl` | string |  |
| `mediaId` | string |  |
| `publishDateTime` | string |  |
| `storyId` | string |  |
| `title` | string |  |
| `topic` | string |  |
| `transcriptUrl` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /:year/:month/:day/:storyId/:slug` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-details.md) for the provider-specific parameters and requirements.

