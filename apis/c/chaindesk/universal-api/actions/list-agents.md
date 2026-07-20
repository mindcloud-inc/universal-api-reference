# Chaindesk: List Agents

Retrieves agents from your Chaindesk workspace.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-agents?${params}`, {
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
| `name` | string | no |  |

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
        "createdAt": "string",
        "iconUrl": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "subscriptions": [
          "string"
        ],
        "updatedAt": "string"
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
| `organization.createdAt` | string |  |
| `organization.iconUrl` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `organization.subscriptions` | array<string> |  |
| `organization.updatedAt` | string |  |
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

Through the native Chaindesk API, this operation is `GET /agents` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

