# echowin: Search Agent Knowledgebase

Finds knowledge base entries in echowin by search query.

```
GET https://connect.mindcloud.co/v1/universal/echowin/latest/actions/search-agent-knowledgebase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a echowin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/search-agent-knowledgebase?connectionId=$CONNECTION_ID&agentId=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echowin/latest/actions/search-agent-knowledgebase?${params}`, {
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
| `agentId` | string | yes |  |
| `query` | string | yes |  |
| `limit` | number | no | Default: `10`. |
| `threshold` | number | no | Default: `0.1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native echowin API returns.

## Native endpoint

Through the native echowin API, this operation is `GET /agents/:agentId/knowledgebase/search` (base URL `https://echo.win/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-agent-knowledgebase.md) for the provider-specific parameters and requirements.

