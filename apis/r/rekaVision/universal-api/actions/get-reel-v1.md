# Reka Vision: Get Reel (V1)

Retrieves a reel generation status from Reka Vision.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-reel-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-reel-v1?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-reel-v1?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "generationConfig": "string",
      "id": "string",
      "output": [
        {}
      ],
      "prompt": "string",
      "renderingConfig": "string",
      "status": "string",
      "updatedAt": "string",
      "videoUrls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp |
| `generationConfig` | string | Generation configuration used |
| `id` | string | Unique identifier for the generation |
| `output` | array<object> | Generated reel outputs |
| `prompt` | string | Prompt used for generation |
| `renderingConfig` | string | Rendering configuration used |
| `status` | string | Current status of the generation |
| `updatedAt` | string | Last update timestamp |
| `videoUrls` | array<string> | List of input video URLs |

## Native endpoint

Through the native Reka Vision API, this operation is `GET /v1/clips/:id` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reel-v1.md) for the provider-specific parameters and requirements.

