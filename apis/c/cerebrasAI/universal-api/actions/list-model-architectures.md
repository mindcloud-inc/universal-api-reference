# Cerebras AI: List Model Architectures

Retrieves model architectures from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-model-architectures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-model-architectures?connectionId=$CONNECTION_ID&orgName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-model-architectures?${params}`, {
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
| `orgName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "modelArchitectures": [
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
| `modelArchitectures` | array<string> |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /management/v1/orgs/:orgName/models` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-model-architectures.md) for the provider-specific parameters and requirements.

