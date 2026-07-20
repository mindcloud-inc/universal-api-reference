# Orq.ai: Create Image Variation

Creates an image variation in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-variation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-variation?connectionId=$CONNECTION_ID&image=string&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image": "string",
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-variation?${params}`, {
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
| `image` | file | yes |  |
| `model` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "data": [
        {
          "url": "https://example.com"
        }
      ],
      "quality": "string",
      "size": "string",
      "usage": {
        "inputTokens": 1,
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
| `created` | number |  |
| `data[].url` | string |  |
| `quality` | string |  |
| `size` | string |  |
| `usage.inputTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/images/variations` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-variation.md) for the provider-specific parameters and requirements.

