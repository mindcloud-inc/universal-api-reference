# Atlassian MCP Universal API Examples

These examples use the MindCloud API key and Atlassian MCP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Initialize Session

Initializes an Atlassian MCP session.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/initialize-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/initialize-session?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Initialize Session action reference](actions/initialize-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlassianMCP/latest/actions/initialize-session).

## Confluence - Create Footer Comment

Creates a Confluence footer comment in Atlassian MCP.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/confluence-create-footer-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlassianMCP/latest/actions/confluence-create-footer-comment', {
  method: 'POST',
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Confluence - Create Footer Comment action reference](actions/confluence-create-footer-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlassianMCP/latest/actions/confluence-create-footer-comment).
