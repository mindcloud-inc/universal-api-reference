# Chaindesk: Create Agent

Creates a new agent in Chaindesk.

```
POST https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "formId": "string",
      "handle": "string",
      "hidden": true,
      "iconUrl": "https://example.com",
      "id": "string",
      "includeSources": true,
      "interfaceConfig": {},
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "nbQueries": 1,
      "organizationId": "string",
      "ownerId": "string",
      "prompt": "string",
      "promptType": "string",
      "restrictKnowledge": true,
      "systemPrompt": "string",
      "temperature": 1,
      "updatedAt": "string",
      "useLanguageDetection": true,
      "useMarkdown": true,
      "userPrompt": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `formId` | string |  |
| `handle` | string |  |
| `hidden` | boolean |  |
| `iconUrl` | string |  |
| `id` | string |  |
| `includeSources` | boolean |  |
| `interfaceConfig` | object |  |
| `modelName` | string |  |
| `name` | string |  |
| `nbQueries` | number |  |
| `organizationId` | string |  |
| `ownerId` | string |  |
| `prompt` | string |  |
| `promptType` | string |  |
| `restrictKnowledge` | boolean |  |
| `systemPrompt` | string |  |
| `temperature` | number |  |
| `updatedAt` | string |  |
| `useLanguageDetection` | boolean |  |
| `useMarkdown` | boolean |  |
| `userPrompt` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `POST /agents` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

