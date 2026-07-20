# AltText.Ai: Update Image

Updates an image in your AltText.Ai library.

```
PUT https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": "string",
  "image": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": "string",
    "image": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetId` | string | yes | The asset ID of the image to update. |
| `image` | object | yes | The image update payload. Provide fields like `alt_text`, `asset_id`, or `metadata` inside this object. |
| `lang` | string | no | One or more language codes to update, such as `en` or `en,fr`. |
| `overwrite` | boolean | no | When true, overwrite existing alt text in the requested language instead of preserving it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "altTexts": {},
      "assetId": "string",
      "createdAt": 1,
      "errorCode": "string",
      "errors": {},
      "metadata": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `altTexts` | object |  |
| `assetId` | string |  |
| `createdAt` | number |  |
| `errorCode` | string |  |
| `errors` | object |  |
| `metadata` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native AltText.Ai API, this operation is `PUT /images/:asset_id` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-image.md) for the provider-specific parameters and requirements.

