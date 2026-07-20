# OpenRouter: Get API Key

Retrieves a specific API key from OpenRouter.

```
GET https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRouter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-api-key?connectionId=$CONNECTION_ID&hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-api-key?${params}`, {
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
| `hash` | string | yes | API key hash identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRouter API returns.

## Native endpoint

Through the native OpenRouter API, this operation is `GET /keys/:hash` (base URL `https://openrouter.ai/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key.md) for the provider-specific parameters and requirements.

