# All Things Considered Podcast: Get Embedded Player Metadata

Retrieves embedded player metadata from All Things Considered Podcast.

```
GET https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-embedded-player-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a All Things Considered Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-embedded-player-metadata?connectionId=$CONNECTION_ID&storyId=nx-s1-5803566&mediaId=nx-s1-9750301" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyId": "nx-s1-5803566",
  "mediaId": "nx-s1-9750301"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/allThingsConsideredPodcast/latest/actions/get-embedded-player-metadata?${params}`, {
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
| `mediaId` | string | yes | Default: `nx-s1-9750301`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioTitle": "string",
      "audioUrl": "https://example.com",
      "available": true,
      "duration": 1,
      "mediaId": "string",
      "seekable": true,
      "slug": "string",
      "slugUrl": "https://example.com",
      "storyId": "string",
      "storyUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioTitle` | string |  |
| `audioUrl` | string |  |
| `available` | boolean |  |
| `duration` | number |  |
| `mediaId` | string |  |
| `seekable` | boolean |  |
| `slug` | string |  |
| `slugUrl` | string |  |
| `storyId` | string |  |
| `storyUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native All Things Considered Podcast API, this operation is `GET /player/embed/:storyId/:mediaId` (base URL `https://www.npr.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-embedded-player-metadata.md) for the provider-specific parameters and requirements.

