# Chaindesk: Delete Agent

Deletes an existing agent from Chaindesk.

```
DELETE https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/delete-agent?${params}`, {
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
      "organization": {
        "id": "string",
        "subscriptions": [
          "string"
        ]
      },
      "organizationId": "string",
      "ownerId": "string",
      "prompt": "string",
      "promptType": "string",
      "restrictKnowledge": true,
      "systemPrompt": "string",
      "temperature": 1,
      "tools": [
        "string"
      ],
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
| `organization` | object |  |
| `organization.id` | string |  |
| `organization.subscriptions` | array<string> |  |
| `organizationId` | string |  |
| `ownerId` | string |  |
| `prompt` | string |  |
| `promptType` | string |  |
| `restrictKnowledge` | boolean |  |
| `systemPrompt` | string |  |
| `temperature` | number |  |
| `tools` | array<string> |  |
| `updatedAt` | string |  |
| `useLanguageDetection` | boolean |  |
| `useMarkdown` | boolean |  |
| `userPrompt` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `DELETE /agents/:agentId` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent.md) for the provider-specific parameters and requirements.

