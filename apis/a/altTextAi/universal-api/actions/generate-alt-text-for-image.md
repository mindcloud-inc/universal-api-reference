# AltText.Ai: Generate Alt Text for Image

Generates alt text for a new image in AltText.Ai.

```
POST https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/generate-alt-text-for-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/generate-alt-text-for-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/generate-alt-text-for-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `async` | boolean | no | When true, queue the image for background processing and return immediately. |
| `gptPrompt` | string | no | Optional English prompt containing `{{AltText}}` to rewrite the generated alt text. |
| `image` | object | yes | The image payload. Provide either a public `url` or base64 `raw` image data, with optional `asset_id`, `tags`, or `metadata` inside this object. |
| `keywords[]` | array<string> | no | Optional SEO keywords or phrases for the generated alt text. |
| `keywordSource` | string | no | Source text to mine for keywords when you do not provide the `keywords` array. |
| `lang` | string | no | One or more language codes, such as `en` or `en,es,fr`, for generated alt text. |
| `maxChars` | number | no | Limit the generated alt text length between 80 and 500 characters. |
| `modelName` | string | no | Choose the AltText.ai language model, such as `describe-regular` or `describe-terse`. |
| `overwrite` | boolean | no | When true, regenerate alt text for an existing image with the same URL or asset ID. |
| `timeoutSecs` | number | no | Maximum seconds to wait for generation, between 5 and 30. |
| `webhookUrl` | string | no | Optional webhook URL override for this request. |

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

Through the native AltText.Ai API, this operation is `POST /images` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-alt-text-for-image.md) for the provider-specific parameters and requirements.

