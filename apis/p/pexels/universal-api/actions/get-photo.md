# Pexels: Get Photo

Retrieves a photo from Pexels by ID.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-photo?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-photo?${params}`, {
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
| `id` | number | yes | Numeric Pexels photo ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "avg_color": "string",
      "height": 1,
      "id": 1,
      "liked": true,
      "photographer": "string",
      "photographer_id": 1,
      "photographer_url": "https://example.com",
      "src": {},
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string | Photo alt text. |
| `avg_color` | string | Average photo color. |
| `height` | number | Photo height in pixels. |
| `id` | number | Pexels photo ID. |
| `liked` | boolean | Whether the authenticated user liked the photo. |
| `photographer` | string | Photographer name. |
| `photographer_id` | number | Photographer ID. |
| `photographer_url` | string | Photographer profile URL. |
| `src` | object | Image source URLs in multiple sizes. |
| `url` | string | Pexels URL for the photo. |
| `width` | number | Photo width in pixels. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/photos/:id` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photo.md) for the provider-specific parameters and requirements.

