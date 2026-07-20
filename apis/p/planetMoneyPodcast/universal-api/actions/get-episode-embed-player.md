# Planet Money Podcast: Get Episode Embed Player

Retrieves the NPR embed player page for a Planet Money episode.

```
GET https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-episode-embed-player
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planet Money Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-episode-embed-player?connectionId=$CONNECTION_ID&storyId=nx-s1-5751177&mediaId=nx-s1-mx-5751177-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyId": "nx-s1-5751177",
  "mediaId": "nx-s1-mx-5751177-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-episode-embed-player?${params}`, {
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
| `storyId` | string | yes | NPR story identifier used by the embed player. Example: `nx-s1-5751177`. |
| `mediaId` | string | yes | NPR media identifier used by the embed player. Example: `nx-s1-mx-5751177-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "data": [
          1
        ],
        "type": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw HTML returned by the public Planet Money embed player page as a Buffer-shaped object. |
| `data.data` | array<number> | HTML bytes returned by NPR. |
| `data.type` | string | Buffer type marker. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Planet Money Podcast API, this operation is `GET https://www.npr.org/player/embed/:storyId/:mediaId` (base URL `https://feeds.npr.org/510289`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode-embed-player.md) for the provider-specific parameters and requirements.

