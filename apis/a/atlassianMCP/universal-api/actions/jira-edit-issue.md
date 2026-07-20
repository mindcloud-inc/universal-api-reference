# Atlassian MCP: Jira - Edit Issue

Updates a Jira issue in Atlassian MCP.

```
PUT https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-edit-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlassian MCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-edit-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-edit-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | no | MCP session ID returned by Atlassian MCP - Initialize Session |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlassian MCP API returns.

## Native endpoint

Through the native Atlassian MCP API, this operation is `POST /mcp` (base URL `https://mcp.atlassian.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/jira-edit-issue.md) for the provider-specific parameters and requirements.

