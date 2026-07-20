# DataBridge: Get Available Models

Retrieves available models from DataBridge.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-available-models?${params}`, {
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
      "chatModels": [
        {}
      ],
      "defaultModels": {},
      "embeddingModels": [
        {}
      ],
      "providers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatModels` | array<object> |  |
| `defaultModels` | object |  |
| `embeddingModels` | array<object> |  |
| `providers` | array<string> |  |

## Native endpoint

Through the native DataBridge API, this operation is `GET /models` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-models.md) for the provider-specific parameters and requirements.

