# Ritekit: Extract Top Image From URL

Retrieves the top image from a URL with Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/extract-top-image-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/extract-top-image-from-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/extract-top-image-from-url?${params}`, {
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
| `url` | string | yes | URL to extract the top image from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": true,
      "top_image": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `result` | boolean |  |
| `top_image` | string |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/image/extract-image` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-top-image-from-url.md) for the provider-specific parameters and requirements.

