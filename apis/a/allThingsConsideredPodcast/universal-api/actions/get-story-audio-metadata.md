# All Things Considered Podcast: Get Story Audio Metadata

Retrieves story audio metadata from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-audio-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-audio-metadata?connectionId=$CONNECTION_ID&year=2026&month=04&day=29&storyId=nx-s1-5803566&slug=musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-story-audio-metadata?${params}`, {
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
      "affiliation": "string",
      "audioUrl": "https://example.com",
      "available": true,
      "duration": 1,
      "mediaId": "string",
      "program": "string",
      "slug": "string",
      "storyId": "string",
      "storyUrl": "https://example.com",
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliation` | string |  |
| `audioUrl` | string |  |
| `available` | boolean |  |
| `duration` | number |  |
| `mediaId` | string |  |
| `program` | string |  |
| `slug` | string |  |
| `storyId` | string |  |
| `storyUrl` | string |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /:year/:month/:day/:storyId/:slug` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-audio-metadata.md) for the provider-specific parameters and requirements.

