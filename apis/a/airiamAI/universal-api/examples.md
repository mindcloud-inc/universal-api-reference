# Airiam AI Universal API Examples

These examples use the MindCloud API key and Airiam AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves a list of workspaces from Airiam AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-workspaces?${params}`, {
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
      "allowChatModelChange": true,
      "chatHistoryRetentionDays": 1,
      "chatHistoryType": "string",
      "contextType": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "models": [
        {}
      ],
      "name": "Ava Chen",
      "sharingType": "string",
      "systemProject": true
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airiamAI/latest/actions/list-workspaces).

## Add Model To Team

Adds a model to the team in Airiam AI.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/add-model-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/add-model-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "active": true,
      "baseModel": "string",
      "chatCredits": 1,
      "contextWindow": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasVision": true,
      "icon": "string",
      "id": "string",
      "imageGen": true,
      "instructionFollowing": true,
      "internalUseOnly": true,
      "maxCompletionTokens": 1,
      "modelRating": 1,
      "name": "Ava Chen",
      "pdfVision": true,
      "promptWrapper": {},
      "settingsAvailable": [
        {}
      ],
      "updated": "2026-05-07T12:00:00.000Z",
      "usesSystemPrompts": true
    }
  ],
  "meta": {}
}
```

See the full [Add Model To Team action reference](actions/add-model-to-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airiamAI/latest/actions/add-model-to-team).
