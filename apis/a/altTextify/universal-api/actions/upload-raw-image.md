# AltTextify: Upload Raw Image

Creates a new image in AltTextify from base64 image data.

```
POST https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/upload-raw-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltTextify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/upload-raw-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "lang": "en",
  "maxChars": "120"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/upload-raw-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "lang": "en",
    "maxChars": "120"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | yes | A base64-encoded image payload, preferably with a data URI prefix. |
| `lang` | string | yes | Language code for generated alt text. Default: `en`. |
| `maxChars` | number | yes | Maximum length of the generated alt text. Default: `120`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt_text": "string",
      "asset_id": "string",
      "async": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "links": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt_text` | string |  |
| `asset_id` | string |  |
| `async` | boolean |  |
| `created_at` | date |  |
| `links` | array<object> |  |

## Native endpoint

Through the native AltTextify API, this operation is `POST /image/raw` (base URL `https://api.alttextify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-raw-image.md) for the provider-specific parameters and requirements.

