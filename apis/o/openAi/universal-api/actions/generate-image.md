# Open AI: Generate Image

Generates an image in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "model": "gpt-image-1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "model": "gpt-image-1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Text prompt describing the image to generate. |
| `model` | list | yes | Image generation model ID. Default: `gpt-image-1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "data": [
        {
          "b64Json": "string"
        }
      ],
      "outputFormat": "string",
      "quality": "string",
      "size": "string",
      "usage": {
        "inputTokens": 1,
        "inputTokensDetails": {
          "imageTokens": 1,
          "textTokens": 1
        },
        "outputTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | string |  |
| `created` | date |  |
| `data[].b64Json` | string |  |
| `outputFormat` | string |  |
| `quality` | string |  |
| `size` | string |  |
| `usage.inputTokens` | number |  |
| `usage.inputTokensDetails.imageTokens` | number |  |
| `usage.inputTokensDetails.textTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/images/generations` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

