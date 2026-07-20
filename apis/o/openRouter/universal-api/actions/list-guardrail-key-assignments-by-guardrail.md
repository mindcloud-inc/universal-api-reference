# OpenRouter: List Guardrail Key Assignments By Guardrail

Retrieves key assignments for a specific guardrail in OpenRouter.

```
GET https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrail-key-assignments-by-guardrail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrail-key-assignments-by-guardrail?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrail-key-assignments-by-guardrail?${params}`, {
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
| `id` | string | yes | Guardrail identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRouter API returns.

## Native endpoint

Through the native OpenRouter API, this operation is `GET /guardrails/:id/assignments/keys` (base URL `https://openrouter.ai/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guardrail-key-assignments-by-guardrail.md) for the provider-specific parameters and requirements.

