# Google AI Studio: List Models

Retrieves available Gemini models from Google AI Studio.

```
GET https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models?${params}`, {
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
      "displayName": "Ava Chen",
      "inputTokenLimit": 1,
      "name": "Ava Chen",
      "outputTokenLimit": 1,
      "supportedGenerationMethods": [
        "string"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Provider model description. |
| `displayName` | string | Human-friendly model name. |
| `inputTokenLimit` | number | Maximum input token count. |
| `name` | string | Model resource name. |
| `outputTokenLimit` | number | Maximum output token count. |
| `supportedGenerationMethods` | array<string> | Supported generation methods for this model. |
| `version` | string | Model version string. |

## Native endpoint

Through the native Google AI Studio API, this operation is `GET v1beta/models` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

