# Simplecast: Get Podcast RSS

Retrieves a podcast RSS feed from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-rss
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-rss?connectionId=$CONNECTION_ID&podcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "podcastId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-rss?${params}`, {
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
| `podcastId` | string | yes | Simplecast podcast identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "rss": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `rss` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /podcasts/:podcast_id/rss` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-rss.md) for the provider-specific parameters and requirements.

