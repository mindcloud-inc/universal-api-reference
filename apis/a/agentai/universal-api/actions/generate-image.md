# Agent.ai: Generate Image

Creates an AI-generated image in Agent.ai.

```
POST https://connect.mindcloud.co/v1/universal/agentai/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "model": "DALL-E 3",
  "modelStyle": "default",
  "modelAspectRatio": "9:16"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentai/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "model": "DALL-E 3",
    "modelStyle": "default",
    "modelAspectRatio": "9:16"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt to generate an image from. |
| `model` | string | yes | Image generation model to use. Default: `DALL-E 3`. |
| `modelStyle` | string | yes | Image style for the generation model. Default: `default`. |
| `modelAspectRatio` | string | yes | Image aspect ratio for the generation model. Default: `9:16`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object | Metadata returned with the generated image. |
| `response` | string | Generated image URL or image response payload. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/generate_image` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

