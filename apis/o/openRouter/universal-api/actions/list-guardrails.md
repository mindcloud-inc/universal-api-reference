# OpenRouter: List Guardrails

Retrieves all configured guardrails from OpenRouter.

```
GET https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-guardrails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRouter API returns.

## Native endpoint

Through the native OpenRouter API, this operation is `GET /guardrails` (base URL `https://openrouter.ai/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guardrails.md) for the provider-specific parameters and requirements.

