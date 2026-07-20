# Langbase: Generate Images



```
POST https://connect.mindcloud.co/v1/universal/langbase/latest/actions/generate-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/generate-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/generate-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string",
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Prompt describing the image to generate. |
| `model` | string | yes | Image model identifier, for example `openai:dall-e-3` or `google:imagen-3.0-generate-002`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `llmApiKey` | string | no | Provider model API key for the `LB-LLM-Key` request header when the selected image model is not already configured in Langbase. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Langbase API returns.

## Native endpoint

Through the native Langbase API, this operation is `POST v1/images` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-images.md) for the provider-specific parameters and requirements.

