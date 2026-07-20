# Kimi: List Models

Retrieves the available models from Kimi.

```
GET https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kimi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kimi/latest/actions/list-models?${params}`, {
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
      "contextLength": 1,
      "created": 1,
      "id": "string",
      "object": "string",
      "ownedBy": "string",
      "parent": "string",
      "permission": [
        {}
      ],
      "root": "string",
      "supportsImageIn": true,
      "supportsReasoning": true,
      "supportsVideoIn": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextLength` | number | Maximum context length. |
| `created` | number | Model creation timestamp. |
| `id` | string | Model ID. |
| `object` | string | Object type, usually model. |
| `ownedBy` | string | Model owner. |
| `parent` | string | Parent model identifier when provided. |
| `permission` | array<object> | Permission metadata for the model. |
| `root` | string | Root model identifier when provided. |
| `supportsImageIn` | boolean | Whether the model supports image input. |
| `supportsReasoning` | boolean | Whether the model supports reasoning. |
| `supportsVideoIn` | boolean | Whether the model supports video input. |

## Native endpoint

Through the native Kimi API, this operation is `GET /v1/models` (base URL `https://api.moonshot.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

