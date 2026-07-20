# Anthropic: Get Model

Retrieves a specific model from Anthropic.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-model?connectionId=$CONNECTION_ID&modelId=claude-sonnet-4-5-20250929" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "claude-sonnet-4-5-20250929"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-model?${params}`, {
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
| `modelId` | string | yes | The model ID. Example: `claude-sonnet-4-5-20250929`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/models/:model_id` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

