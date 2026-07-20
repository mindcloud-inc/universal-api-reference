# Atlassian MCP: Jira - List Project Issue Types

Retrieves Jira project issue types from Atlassian MCP.

```
GET https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-list-project-issue-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlassian MCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-list-project-issue-types?connectionId=$CONNECTION_ID&sessionId=string&cloudId=string&projectIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "cloudId": "string",
  "projectIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/jira-list-project-issue-types?${params}`, {
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
| `sessionId` | string | yes | MCP session ID returned by Atlassian MCP - Initialize Session. |
| `cloudId` | string | yes | Atlassian cloud ID for the target site. |
| `projectIdOrKey` | string | yes | Jira project ID or project key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlassian MCP API returns.

## Native endpoint

Through the native Atlassian MCP API, this operation is `POST /mcp` (base URL `https://mcp.atlassian.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/jira-list-project-issue-types.md) for the provider-specific parameters and requirements.

