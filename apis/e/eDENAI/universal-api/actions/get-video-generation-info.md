# EDEN AI: Get Video Generation Info

Retrieves feature information for video generation in EDEN AI.

```
GET https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-video-generation-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-video-generation-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-video-generation-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endpoints": {
        "create": "string",
        "delete": "string",
        "get": "string",
        "list": "string"
      },
      "feature": "string",
      "inputSchema": {
        "fields": [
          {}
        ]
      },
      "mode": "string",
      "models": [
        {
          "model": "string",
          "regions": [
            {
              "code": "string",
              "name": "Ava Chen"
            }
          ]
        }
      ],
      "outputSchema": {
        "fields": [
          {}
        ]
      },
      "subfeature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Subfeature description. |
| `endpoints` | object | Available endpoint operations for the subfeature. |
| `endpoints.create` | string | Create endpoint for submitting an async video generation job. |
| `endpoints.delete` | string | Endpoint for deleting an async video generation job. |
| `endpoints.get` | string | Endpoint for retrieving an async video generation job. |
| `endpoints.list` | string | Endpoint for listing async video generation jobs. |
| `feature` | string | Top-level Eden AI feature category. |
| `inputSchema` | object | Input schema for the video generation action. |
| `inputSchema.fields` | array<object> | Supported input fields. |
| `mode` | string | Execution mode for the subfeature. |
| `models` | array<object> | Provider models available for the subfeature. |
| `models[].model` | string | Provider model identifier. |
| `models[].regions` | array<object> | Regions supported by the model. |
| `models[].regions[].code` | string | Region code. |
| `models[].regions[].name` | string | Region name. |
| `outputSchema` | object | Output schema for video generation results. |
| `outputSchema.fields` | array<object> | Top-level output fields. |
| `subfeature` | string | Specific Eden AI subfeature key. |

## Native endpoint

Through the native EDEN AI API, this operation is `GET /info/video/generation_async` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-generation-info.md) for the provider-specific parameters and requirements.

