# Atlassian MCP: Confluence - List Spaces

Retrieves Confluence spaces from Atlassian MCP.

```
GET https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/confluence-list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atlassian MCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/confluence-list-spaces?connectionId=$CONNECTION_ID&sessionId=string&cloudId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "cloudId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/confluence-list-spaces?${params}`, {
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
| `sessionId` | string | yes | MCP session ID returned by Atlassian MCP - Initialize Session |
| `cloudId` | string | yes |  |
| `ids` | string | no |  |
| `keys` | string | no |  |
| `type` | string | no |  |
| `status` | string | no |  |
| `labels` | string | no |  |
| `favourite` | boolean | no |  |
| `favoritedBy` | string | no |  |
| `expand` | string | no |  |
| `start` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Atlassian MCP API returns.

## Native endpoint

Through the native Atlassian MCP API, this operation is `POST /mcp` (base URL `https://mcp.atlassian.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confluence-list-spaces.md) for the provider-specific parameters and requirements.

