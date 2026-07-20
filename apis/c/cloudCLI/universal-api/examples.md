# Cloud CLI Universal API Examples

These examples use the MindCloud API key and Cloud CLI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List AI Agent Models

Retrieves supported AI agent models from Cloud CLI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-ai-agent-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-ai-agent-models?${params}`, {
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
  "data": [
    {
      "defaultModel": "string",
      "options": [
        {
          "label": "string",
          "value": "string"
        }
      ],
      "provider": "string"
    }
  ],
  "meta": {}
}
```

See the full [List AI Agent Models action reference](actions/list-ai-agent-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudCLI/latest/actions/list-ai-agent-models).

## Create Environment

Creates a new environment in Cloud CLI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/create-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "My Backend API",
  "subdomain": "mybackend-abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/create-environment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "My Backend API",
    "subdomain": "mybackend-abc123"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accessUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "githubUrl": "https://example.com",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string",
      "subdomain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Environment action reference](actions/create-environment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudCLI/latest/actions/create-environment).
