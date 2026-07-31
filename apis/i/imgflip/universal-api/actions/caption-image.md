# Imgflip: Caption Image



```
POST https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/caption-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imgflip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/caption-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "text0": "string",
  "text1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/caption-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "text0": "string",
    "text1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template ID returned by List Popular Memes. |
| `text0` | string | yes | Top caption text. Do not use with boxes. |
| `text1` | string | yes | Bottom caption text. Do not use with boxes. |
| `font` | string | no | Optional font family. Imgflip defaults to impact. |
| `maxFontSize` | number | no | Optional maximum font size in pixels. Imgflip defaults to 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page_url` | string | Public Imgflip image page URL. |
| `url` | string | Public generated image URL. |

## Native endpoint

Through the native Imgflip API, this operation is `POST /caption_image` (base URL `https://api.imgflip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/caption-image.md) for the provider-specific parameters and requirements.

