# Relevance AI: Delete Tool



```
DELETE https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/delete-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/delete-tool?connectionId=$CONNECTION_ID&toolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "toolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/delete-tool?${params}`, {
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
| `toolId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Relevance AI API returns.

## Native endpoint

Through the native Relevance AI API, this operation is `POST /studios/bulk_delete` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tool.md) for the provider-specific parameters and requirements.

