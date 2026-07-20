# Stability AI: Fetch Async Generation Result

Retrieves an asynchronous generation result from Stability AI.

```
GET https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result?connectionId=$CONNECTION_ID&id=generation-result-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "generation-result-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result?${params}`, {
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
| `id` | string | yes | The async generation result id returned by Stability AI. Example: `generation-result-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish_reason": "string",
      "id": "string",
      "image": "string",
      "seed": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish_reason` | string | Reason the generation finished when available. |
| `id` | string | Asynchronous generation result identifier when the job is still in progress. |
| `image` | string | Generated image encoded as base64 when the job is complete. |
| `seed` | number | Seed used for the generation when available. |
| `status` | string | Asynchronous generation status when the job is still in progress. |

## Native endpoint

Through the native Stability AI API, this operation is `GET /v2beta/results/[:id]` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-async-generation-result.md) for the provider-specific parameters and requirements.

