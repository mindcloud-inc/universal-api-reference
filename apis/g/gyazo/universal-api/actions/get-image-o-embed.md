# Gyazo: Get Image OEmbed

Retrieves oEmbed data for a Gyazo image.

```
GET https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image-o-embed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image-o-embed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fgyazo.com%2F8980c52421e452ac3355ca3e5cfe7a0c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://gyazo.com/8980c52421e452ac3355ca3e5cfe7a0c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-image-o-embed?${params}`, {
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
| `url` | string | yes | The Gyazo image page URL to resolve through oEmbed. Example: `https://gyazo.com/8980c52421e452ac3355ca3e5cfe7a0c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
      "provider_name": "Ava Chen",
      "provider_url": "https://example.com",
      "type": "string",
      "url": "https://example.com",
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
| `height` | number |  |
| `provider_name` | string |  |
| `provider_url` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Gyazo API, this operation is `GET /api/oembed` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-o-embed.md) for the provider-specific parameters and requirements.

