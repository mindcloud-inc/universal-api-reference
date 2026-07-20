# Typeform: Create Image



```
POST https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typeform/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | no | File name for the uploaded image. |
| `image` | string | no | Image payload. |
| `url` | string | no | Public URL of the image. |

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

Through the native Typeform API, this operation is `POST /images` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

