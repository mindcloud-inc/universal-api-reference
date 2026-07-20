# Typeform: List Images



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/list-images?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avgColor": "string",
      "fileName": "Ava Chen",
      "hasAlpha": true,
      "height": 1,
      "id": "string",
      "mediaType": "string",
      "src": "string",
      "uploadSource": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgColor` | string | Average image color. |
| `fileName` | string | Image file name. |
| `hasAlpha` | boolean | Whether image has alpha channel. |
| `height` | number | Image height in pixels. |
| `id` | string | Image ID. |
| `mediaType` | string | Image media type. |
| `src` | string | Image source URL. |
| `uploadSource` | string | Upload source. |
| `width` | number | Image width in pixels. |

## Native endpoint

Through the native Typeform API, this operation is `GET /images` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-images.md) for the provider-specific parameters and requirements.

