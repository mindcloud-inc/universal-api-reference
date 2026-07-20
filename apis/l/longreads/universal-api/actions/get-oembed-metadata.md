# Longreads: Get OEmbed Metadata

Retrieves Longreads oEmbed metadata for a URL.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-oembed-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-oembed-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-oembed-metadata?${params}`, {
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
| `url` | string | yes | The public URL to generate oEmbed metadata for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_name": "Ava Chen",
      "author_url": "https://example.com",
      "height": 1,
      "html": "string",
      "provider_name": "Ava Chen",
      "provider_url": "https://example.com",
      "thumbnail_url": "https://example.com",
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
| `author_name` | string |  |
| `author_url` | string |  |
| `height` | number |  |
| `html` | string |  |
| `provider_name` | string |  |
| `provider_url` | string |  |
| `thumbnail_url` | string |  |
| `title` | string |  |
| `type` | string |  |
| `version` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /oembed/1.0/embed` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oembed-metadata.md) for the provider-specific parameters and requirements.

