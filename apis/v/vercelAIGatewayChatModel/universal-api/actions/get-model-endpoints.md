# Vercel AI Gateway Chat Model: Get Model Endpoints

Retrieves provider endpoints for a specific Vercel AI Gateway model.

```
GET https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-model-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel AI Gateway Chat Model `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-model-endpoints?connectionId=$CONNECTION_ID&creator=string&model=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "creator": "string",
  "model": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercelAIGatewayChatModel/latest/actions/get-model-endpoints?${params}`, {
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
| `creator` | string | yes | Model creator slug, such as google or openai. |
| `model` | string | yes | Model slug without the creator prefix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "architecture": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endpoints": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "releasedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `architecture` | object | Architecture metadata including modalities. |
| `createdAt` | date | Model creation timestamp. |
| `description` | string | Provider description of the model. |
| `endpoints` | array<object> | Available provider endpoints for this model. |
| `id` | string | Fully qualified model identifier. |
| `name` | string | Human-readable model name. |
| `releasedAt` | date | Model release timestamp. |

## Native endpoint

Through the native Vercel AI Gateway Chat Model API, this operation is `GET /models/:creator/:model/endpoints` (base URL `https://ai-gateway.vercel.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-endpoints.md) for the provider-specific parameters and requirements.

