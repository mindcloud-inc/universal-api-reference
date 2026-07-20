# Lex Fridman Podcast: Get OEmbed Embed

Retrieves oEmbed data for a URL from Lex Fridman Podcast.

```
GET https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-embed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lex Fridman Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-embed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Flexfridman.com%2Fpodcast%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://lexfridman.com/podcast/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-oembed-embed?${params}`, {
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
| `url` | string | yes | The resource URL to embed. Default: `https://lexfridman.com/podcast/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorName": "Ava Chen",
      "authorUrl": "https://example.com",
      "height": 1,
      "html": "string",
      "providerName": "Ava Chen",
      "providerUrl": "https://example.com",
      "title": "string",
      "type": "string",
      "version": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorName` | string |  |
| `authorUrl` | string |  |
| `height` | number |  |
| `html` | string |  |
| `providerName` | string |  |
| `providerUrl` | string |  |
| `title` | string |  |
| `type` | string |  |
| `version` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Lex Fridman Podcast API, this operation is `GET /wp-json/oembed/1.0/embed` (base URL `https://lexfridman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oembed-embed.md) for the provider-specific parameters and requirements.

