# Simplecast: Get OEmbed

Retrieves oEmbed data from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-oembed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-oembed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-oembed?${params}`, {
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
| `url` | string | yes | Podcast or episode URL to embed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
      "html": "string",
      "title": "string",
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
| `html` | string |  |
| `title` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /oembed` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oembed.md) for the provider-specific parameters and requirements.

