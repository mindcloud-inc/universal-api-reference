# OpenRouter: List Model Endpoints

Retrieves endpoints for a specific model in OpenRouter.

```
GET https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-model-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-model-endpoints?connectionId=$CONNECTION_ID&author=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "author": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/list-model-endpoints?${params}`, {
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
| `author` | string | yes | Model author segment used in the path. |
| `slug` | string | yes | Model slug segment used in the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRouter API returns.

## Native endpoint

Through the native OpenRouter API, this operation is `GET /models/:author/:slug/endpoints` (base URL `https://openrouter.ai/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-model-endpoints.md) for the provider-specific parameters and requirements.

