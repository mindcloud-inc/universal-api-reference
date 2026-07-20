# Groq: Delete Model

Deletes a model from Groq.

```
DELETE https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-model?${params}`, {
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
| `modelId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Groq API returns.

## Native endpoint

Through the native Groq API, this operation is `DELETE /openai/v1/models/:model` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-model.md) for the provider-specific parameters and requirements.

