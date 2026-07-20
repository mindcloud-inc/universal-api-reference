# Sellfy: Get oEmbed

Retrieves oEmbed data from Sellfy for a store or product URL.

```
GET https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sellfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fdemo.sellfy.store%2Fp%2Fbottle-mockup%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://demo.sellfy.store/p/bottle-mockup/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sellfy/latest/actions/get-oembed?${params}`, {
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
| `url` | string | yes | The product or store page URL to convert into oEmbed data. Example: `https://demo.sellfy.store/p/bottle-mockup/`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorName": "Ava Chen",
      "authorUrl": "https://example.com",
      "html": "string",
      "id": "string",
      "providerName": "Ava Chen",
      "providerUrl": "https://example.com",
      "thumbnailHeight": 1,
      "thumbnailUrl": "https://example.com",
      "thumbnailWidth": 1,
      "title": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorName` | string | Name of the Sellfy store that owns the embedded resource. |
| `authorUrl` | string | Store URL for the embedded resource. |
| `html` | string | Embed HTML returned by Sellfy. |
| `id` | string | Sellfy product identifier when the URL points to a product. |
| `providerName` | string | Resource provider name. |
| `providerUrl` | string | Resource provider URL. |
| `thumbnailHeight` | number | Thumbnail height for product embeds when provided. |
| `thumbnailUrl` | string | Thumbnail image URL for product embeds when provided. |
| `thumbnailWidth` | number | Thumbnail width for product embeds when provided. |
| `title` | string | Product or store title. |
| `type` | string | Embedded resource type, such as product or store. |
| `version` | string | oEmbed version. |

## Native endpoint

Through the native Sellfy API, this operation is `GET /oembed/` (base URL `https://sellfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oembed.md) for the provider-specific parameters and requirements.

