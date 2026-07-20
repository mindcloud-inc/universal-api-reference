# Ringg AI Universal API Examples

These examples use the MindCloud API key and Ringg AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace Info

Retrieves workspace information from Ringg AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-workspace-info?${params}`, {
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
      "workspaceInfo": {
        "apiKey": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "credits": 1,
        "id": "string",
        "lockedCredits": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Workspace Info action reference](actions/get-workspace-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ringgAI/latest/actions/get-workspace-info).

## Create Agent

Creates an agent in Ringg AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentName": "Ava Chen",
  "introductionAndObjective": "string",
  "responseGuidelines": "string",
  "task": "string",
  "primaryLanguage": "string",
  "voiceId": "string",
  "introMessage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentName": "Ava Chen",
    "introductionAndObjective": "string",
    "responseGuidelines": "string",
    "task": "string",
    "primaryLanguage": "string",
    "voiceId": "string",
    "introMessage": "string"
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
      "data": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "version": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ringgAI/latest/actions/create-agent).
