# Vercel AI Gateway Chat Model: List Models

Retrieves available models from Vercel AI Gateway.

```
GET https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel AI Gateway Chat Model `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/list-models?${params}`, {
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
      "contextWindow": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "maxTokens": 1,
      "name": "Ava Chen",
      "ownedBy": "string",
      "releasedAt": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextWindow` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `maxTokens` | number |  |
| `name` | string |  |
| `ownedBy` | string |  |
| `releasedAt` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Vercel AI Gateway Chat Model API, this operation is `GET /models` (base URL `https://ai-gateway.vercel.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

