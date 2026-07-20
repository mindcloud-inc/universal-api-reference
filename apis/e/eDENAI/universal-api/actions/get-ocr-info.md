# EDEN AI: Get OCR Info

Retrieves feature information for OCR in EDEN AI.

```
GET https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-ocr-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-ocr-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-ocr-info?${params}`, {
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
        "create": "string"
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
| `endpoints.create` | string | Create endpoint for executing the subfeature. |
| `feature` | string | Top-level Eden AI feature category. |
| `inputSchema` | object | Input schema for the OCR action. |
| `inputSchema.fields` | array<object> | Supported input fields. |
| `mode` | string | Execution mode for the subfeature. |
| `models` | array<object> | Provider models available for the subfeature. |
| `models[].model` | string | Provider model identifier. |
| `models[].regions` | array<object> | Regions supported by the model. |
| `models[].regions[].code` | string | Region code. |
| `models[].regions[].name` | string | Region name. |
| `outputSchema` | object | Output schema for OCR results. |
| `outputSchema.fields` | array<object> | Top-level output fields. |
| `subfeature` | string | Specific Eden AI subfeature key. |

## Native endpoint

Through the native EDEN AI API, this operation is `GET /info/ocr/ocr` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ocr-info.md) for the provider-specific parameters and requirements.

