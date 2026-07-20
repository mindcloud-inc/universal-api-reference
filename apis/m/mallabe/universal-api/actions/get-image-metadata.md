# Mallabe: Get Image Metadata

Retrieves metadata for an image from Mallabe.

```
GET https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/get-image-metadata?${params}`, {
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
| `url` | string | yes | Publicly accessible image URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": 1,
      "density": 1,
      "depth": "string",
      "format": "string",
      "hasAlpha": true,
      "hasProfile": true,
      "height": 1,
      "isProgressive": true,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | number |  |
| `density` | number |  |
| `depth` | string |  |
| `format` | string |  |
| `hasAlpha` | boolean |  |
| `hasProfile` | boolean |  |
| `height` | number |  |
| `isProgressive` | boolean |  |
| `width` | number |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /images/metadata` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-metadata.md) for the provider-specific parameters and requirements.

