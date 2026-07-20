# Vadootv: Get character image

Retrieves a generated character image URL from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-character-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-character-image?connectionId=$CONNECTION_ID&id=Image%20generation%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "Image generation ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-character-image?${params}`, {
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
| `id` | string | yes | The image ID returned by the character image generation endpoint. Example: `Image generation ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Character image generation status. |
| `url` | string | Character image URL when available. |

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_character_image` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character-image.md) for the provider-specific parameters and requirements.

